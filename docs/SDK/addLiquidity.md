---
sidebar_position: 2
sidebar_label: Adding Liquidity
---

# Adding Liquidity

This guide shows how to add liquidity into a pool using the SDK and massa-web3. In this example, we will be adding 20 USDC and 5 WMAS into a Pair of USDC/WMAS/20bps

## 1. Required imports for this guide

```ts
import {
  ChainId,
  IERC20,
  IRouter,
  LB_ROUTER_ADDRESS,
  LiquidityDistribution,
  PairV2,
  TokenAmount,
  WMAS as _WMAS,
  USDC as _USDC,
  parseUnits,
  Percent,
  ILBPair
} from '@dusalabs/sdk'
import { Account, Web3Provider } from '@massalabs/massa-web3'
```

## 2. Declare required constants

```ts

const logEvents = (client: Web3Provider, txId: string): void => {
  client
    .getEvents({ operationId: txId })
    .then((r) => r.forEach((e) => console.log(e.data)))
}

const createClient = async (baseAccount: Account, mainnet = false) =>
  mainnet
    ? Web3Provider.mainnet(baseAccount)
    : Web3Provider.buildnet(baseAccount)

const privateKey = process.env.PRIVATE_KEY
if (!privateKey) throw new Error('Missing PRIVATE_KEY in .env file')
const account = await Account.fromPrivateKey(privateKey)
if (!account.address) throw new Error('Missing address in account')
const client = await createClient(account)
const CHAIN_ID = ChainId.BUILDNET
```

Note that in your project, you most likely will not hardcode the private key at any time. You would be using libraries like [wallet-provider](https://github.com/massalabs/wallet-provider) to connect to a wallet, sign messages, interact with contracts, and get the above constants.

```ts
// initialize tokens
const WMAS = _WMAS[CHAIN_ID];
const USDC = _USDC[CHAIN_ID];

const router = LB_ROUTER_ADDRESS[CHAIN_ID];
```

## 3. Declare user inputs and initialize `TokenAmount`

```ts
// user string input; in this case representing 20 USDC and 20 WMAS
const typedValueUSDC = '20'
const typedValueWMAS = '20'

// parse user input into decimal precision, which is 6 for USDC and 9 for WMAS
const tokenAmountUSDC = new TokenAmount(USDC, parseUnits(typedValueUSDC, USDC.decimals));
const tokenAmountWMAS = new TokenAmount(WMAS, parseUnits(typedValueWMAS, WMAS.decimals));

// set amount slippage tolerance
const allowedAmountSlippage = 50; // in bips, 0.5% in this case

// set price slippage tolerance
const allowedPriceSlippage = 50; // in bips, 0.5% in this case

// set deadline for the transaction
const currentTimeInMs = new Date().getTime();
const deadline = currentTimeInMs + 3_600_000;
```

## 4. Get the LBPair's active bin

```ts
const pair = new PairV2(USDC, WMAS);
const binStep = 20;
const lbPair = await pair.fetchLBPair(binStep, client, CHAIN_ID);
const lbPairData = await new ILBPair(lbPair.LBPair, client).getReservesAndId();
```

## 5. Get addLiquidity parameters

```ts
const addLiquidityInput = await pair.addLiquidityParameters(
  lbPair.LBPair,
  binStep,
  tokenAmountUSDC,
  tokenAmountWMAS,
  new Percent(BigInt(allowedAmountSlippage), 10_000n),
  new Percent(BigInt(allowedPriceSlippage), 10_000n),
  LiquidityDistribution.SPOT,
  client
);

const params = pair.liquidityCallParameters({
  ...addLiquidityInput,
  activeIdDesired: lbPairData.activeId,
  to: account.address.toString(),
  deadline,
});
```

## 6. Execute contract call

```ts
// increase allowance for the router
const approveTxId1 = await new IERC20(USDC.address, client).approve(router, tokenAmountUSDC.raw);
const approveTxId2 = await new IERC20(WMAS.address, client).approve(router, tokenAmountWMAS.raw);

if (approveTxId1) await approveTxId1.waitSpeculativeExecution()
if (approveTxId2) await approveTxId2.waitSpeculativeExecution()

// add liquidity
const txId = await new IRouter(router, client).add(params);
console.log("txId", txId);

// await transaction confirmation and log output events
await txId.waitSpeculativeExecution()
await client
  .smartContracts()
  .getFilteredScOutputEvents({
    emitter_address: null,
    start: null,
    end: null,
    original_caller_address: null,
    is_final: null,
    original_operation_id: txId,
  })
  .then((r) =>
    r.forEach(({ data }) => {
      if (data.startsWith("DEPOSITED_TO_BIN:")) console.log(EventDecoder.decodeLiquidity(data));
      else console.log(data);
    })
  );
```
