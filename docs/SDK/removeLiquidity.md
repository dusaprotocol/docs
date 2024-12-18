---
sidebar_position: 3
sidebar_label: Removing Liquidity
---

# Removing Liquidity

This guide shows how to remove liquidity from a pool using the SDK and massa-web3. In this example, we will be removing liquidity from a LBPair of USDC/WMAS/20bps

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

## 3. Getting data

### LBPair and active bin

```ts
const pair = new PairV2(USDC, WMAS);
const binStep = 20;
const lbPair = await pair.fetchLBPair(binStep, client, CHAIN_ID);
const pairAddress = lbPair.LBPair;
const pairContract = new ILBPair(pairAddress, client);
const lbPairData = await pairContract.getReservesAndId();
const tokens = await pairContract.getTokens()
const activeBinId = lbPairData.activeId;
```

### Liquidity positions

```ts
const userPositionIds = await pairContract.getUserBinIds(address);
const addressArray = Array.from({ length: userPositionIds.length }, () => address);
const bins = await pairContract.getBins(userPositionIds);

const allBins = await pairContract.balanceOfBatch(addressArray, userPositionIds);
const nonZeroAmounts = allBins.filter((amount) => amount !== 0n);
const totalSupplies = await pairContract.getSupplies(userPositionIds);
```

## 4. Grant LBRouter access to your LBTokens

```ts
const approved = await pairContract.isApprovedForAll(address, router);
if (!approved) {
  const txIdApprove = await pairContract.setApprovalForAll(router, true);
  console.log("txIdApprove", txIdApprove);
}
```

## 5. Set removeLiquidity parameters

```ts
const currentTimeInMs = new Date().getTime();
const deadline = currentTimeInMs + 3_600_000;

// set amount slippage tolerance
const allowedAmountSlippage = 50; // in bips, 0.5% in this case

const removeLiquidityInput = pair.calculateAmountsToRemove(
  userPositionIds,
  activeBinId,
  bins,
  totalSupplies,
  nonZeroAmounts.map(String),
  new Percent(BigInt(allowedAmountSlippage), 10_000n)
);

const params = pair.liquidityCallParameters({
  ...removeLiquidityInput,
  amount0Min: removeLiquidityInput.amountXMin,
  amount1Min: removeLiquidityInput.amountYMin,
  ids: userPositionIds,
  amounts: nonZeroAmounts,
  token0: tokens[0],
  token1: tokens[1],
  binStep,
  to: address,
  deadline,
});
```

## 6. Execute contract call

```ts
const txId = await new IRouter(router, client).remove(params);
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
      if (data.startsWith("WITHDRAWN_FROM_BIN:")) console.log(EventDecoder.decodeLiquidity(data));
      else console.log(data);
    })
  );
```
