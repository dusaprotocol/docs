---
sidebar_position: 1
sidebar_label: Making a Trade
---

# Making a Trade

This guide demonstrates how to execute a swap. In this example, we will be swapping 20 USDC for WETH.

## 1. Required imports for this guide

```ts
import {
  ChainId,
  IERC20,
  IRouter,
  LB_ROUTER_ADDRESS,
  Percent,
  TokenAmount,
  DAI as _DAI,
  USDC as _USDC,
  WETH as _WETH,
  WMAS as _WMAS,
  parseUnits,
  QuoterHelper
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
const router = LB_ROUTER_ADDRESS[CHAIN_ID]
```

Note that in your project, you most likely will not hardcode the private key at any time. You would be using libraries like [wallet-provider](https://github.com/massalabs/wallet-provider) to connect to a wallet, sign messages, interact with contracts, and get the above constants.

```ts
// initialize tokens
const WMAS = _WMAS[CHAIN_ID];
const USDC = _USDC[CHAIN_ID];
const WETH = _WETH[CHAIN_ID];
```

## 3. Declare user inputs and initialize `TokenAmount`

```ts
// the input token in the trade
const inputToken = WMAS;

// the output token in the trade
const outputToken = WETH;

// specify whether user gave an exact inputToken or outputToken value for the trade
const isExactIn = true;

// user string input; in this case representing 20 USDC
const typedValueIn = "20";

// parse user input into inputToken's decimal precision, which is 6 for USDC
const typedValueInParsed = parseUnits(typedValueIn, inputToken.decimals).toString(); // returns 20000000

// wrap into TokenAmount
const amountIn = new TokenAmount(inputToken, typedValueInParsed);

const maxHops = 3
```

## 4. Get the best trade

```ts
const isNativeIn = true;   // set to 'true' if swapping from MAS; otherwise, 'false'
const isNativeOut = false; // set to 'true' if swapping to MAS; otherwise, 'false'

const bestTrade = await QuoterHelper.findBestPath(
    inputToken,
    isNativeIn,
    outputToken,
    isNativeOut,
    amountIn,
    isExactIn,
    maxHops,
    client,
    CHAIN_ID
  )
```

## 6. Check trade information

```ts
// print useful information about the trade, such as the quote, executionPrice, fees, etc
console.log(bestTrade.toLog());

if (!bestTrade || !executeSwap) return

// get trade fee information
const { totalFeePct, feeAmountIn } = bestTrade.getTradeFee();
console.log("Total fees percentage", totalFeePct.toSignificant(6), "%");
console.log(`Fee: ${feeAmountIn.toSignificant(6)} ${feeAmountIn.token.symbol}`);
```

## 7. Declare slippage tolerance and swap method/parameters

```ts
// set slippage tolerance
const userSlippageTolerance = new Percent(1n, 100n); // 1%

// generate swap method and parameters for contract call
const params = bestTrade.swapCallParameters({
    ttl: 1000 * 60 * 10, // 10 minutes
    recipient: account.address.toString(),
    allowedSlippage: userSlippageTolerance
  })
```

## 8. Execute trade using massa-web3

```ts
// increase allowance for the router (not needed if inputToken is MAS)
const txIdAllowance = await new IERC20(inputToken.address, client).approve(
  router,
  bestTrade.inputAmount.raw
)

if (txIdAllowance) {
  console.log('txIdAllowance', txIdAllowance)
  await txIdAllowance.waitSpeculativeExecution()
  logEvents(client, txIdAllowance.id)
}

// execute swap
const txId = await new IRouter(router, client).swap(params)
console.log('txId', txId.id)

// await tx confirmation and log events
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
    r.forEach(({data}) => {
      if (data.startsWith("SWAP:")) console.log(EventDecoder.decodeSwap(data));
      else console.log(data);
    });
  );
```
