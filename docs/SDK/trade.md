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
  IRouter,
  LB_ROUTER_ADDRESS,
  PairV2,
  Percent,
  RouteV2,
  Token,
  TokenAmount,
  TradeV2,
  WMAS as _WMAS,
  parseUnits
} from '@dusalabs/sdk'
import {
  ClientFactory,
  EOperationStatus,
  ProviderType,
  WalletClient
} from '@massalabs/massa-web3'
```

## 2. Declare required constants
```ts
const BUILDNET_URL = 'https://buildnet.massa.net/api/v2'
const privateKey = process.env.PRIVATE_KEY
if (!privateKey) throw new Error('Missing PRIVATE_KEY in .env file')
const account = await WalletClient.getAccountFromSecretKey(privateKey)
if (!account.address) throw new Error('Missing address in account')
const client = await ClientFactory.createCustomClient(
  [
    { url: BUILDNET_URL, type: ProviderType.PUBLIC },
    { url: BUILDNET_URL, type: ProviderType.PRIVATE }
  ],
  true,
  account
)
```
Note that in your project, you most likely will not hardcode the private key at any time. You would be using libraries like [wallet-provider](https://github.com/massalabs/wallet-provider) to connect to a wallet, sign messages, interact with contracts, and get the above constants.

```ts
// initialize tokens
const WMAS = _WMAS[ChainId.BUILDNET]
const USDC = new Token(
  ChainId.BUILDNET,
  'AS127XuJBNCJrQafhVy8cWPfxSb4PV7GFueYgAEYCEPJy3ePjMNb8',
  9,
  'USDC',
  'USD Coin'
)
const WETH = new Token(
  ChainId.BUILDNET,
  'AS12WuZMkAEeDGczFtHYDSnwJvmXwrUWtWo4GgKYUaR2zWv3X6RHG',
  9,
  'WETH',
  'Wrapped Ether'
)

// declare bases used to generate trade routes
const BASES = [WMAS, USDC, WETH] 
```

## 3. Declare user inputs and initialize `TokenAmount`
```ts
// the input token in the trade
const inputToken = USDC

// the output token in the trade
const outputToken = WMAS

// specify whether user gave an exact inputToken or outputToken value for the trade
const isExactIn = true

// user string input; in this case representing 20 USDC
const typedValueIn = '20' 

// parse user input into inputToken's decimal precision, which is 6 for USDC
const typedValueInParsed = parseUnits( 
  typedValueIn, 
  inputToken.decimals
).toString() // returns 20000000

// wrap into TokenAmount
const amountIn = new TokenAmount(inputToken, typedValueInParsed)
```

## 4. Use PairV2 and RouteV2 functions to generate all possible routes
```ts
// get all [Token, Token] combinations 
const allTokenPairs = PairV2.createAllTokenPairs(
  inputToken,
  outputToken,
  BASES
)

// init PairV2 instances for the [Token, Token] pairs
const allPairs = PairV2.initPairs(allTokenPairs) 

// generates all possible routes to consider
const allRoutes = RouteV2.createAllRoutes(
  allPairs,
  inputToken,
  outputToken,
  2 // maxHops 
) 
```

## 5. Generate TradeV2 instances and get the best trade
```ts
const isMasIn = false // set to 'true' if swapping from MAS; otherwise, 'false'
const isMasOut = true // set to 'true' if swapping to MAS; otherwise, 'false'

// generates all possible TradeV2 instances
const chainId = ChainId.BUILDNET
const trades = await TradeV2.getTradesExactIn(
  allRoutes,
  amountIn,
  outputToken,
  isMasIn,
  isMasOut, 
  provider,
  chainId
) 

// chooses the best trade 
const bestTrade = TradeV2.chooseBestTrade(trades, isExactIn)
```

## 6. Check trade information
```ts
// print useful information about the trade, such as the quote, executionPrice, fees, etc
console.log(bestTrade.toLog())

// get trade fee information
const { totalFeePct, feeAmountIn } = bestTrade.getTradeFee()
console.log('Total fees percentage', totalFeePct.toSignificant(6), '%')
console.log(`Fee: ${feeAmountIn.toSignificant(6)} ${feeAmountIn.token.symbol}`)
```

## 7. Declare slippage tolerance and swap method/parameters
```ts
// set slippage tolerance
const userSlippageTolerance = new Percent(BigInt(50), BigInt(10000)) // 0.5%

// set deadline for the transaction
const currenTimeInSec =  Math.floor((new Date().getTime()) / 1000)
const deadline = currenTimeInSec + 3600 // 1 hour

// set swap options
const swapOptions = {
  recipient: account.address, 
  allowedSlippage: userSlippageTolerance, 
  deadline,
  feeOnTransfer: false // or true
}

// generate swap method and parameters for contract call
const {
  methodName, // e.g. swapExactTokensForMAS,
  args,       // e.g.[amountIn, amountOut, binSteps, path, to, deadline]
  value       // e.g. 0x0
} = bestTrade.swapCallParameters(swapOptions)

```
## 8. Execute trade using massa-web3
```ts
// init router contract
const router = new IRouter(LB_ROUTER_ADDRESS[chainId], client)

// execute swap
const txId = await router[params.methodName](params)
console.log('txId', txId)
```