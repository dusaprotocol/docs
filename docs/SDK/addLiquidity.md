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
  ILBPair,
} from "@dusalabs/sdk";
import {
  BUILDNET_CHAIN_ID,
  ClientFactory,
  DefaultProviderUrls,
  ProviderType,
  WalletClient,
} from "@massalabs/massa-web3";
```

## 2. Declare required constants

```ts
const BUILDNET_URL = DefaultProviderUrls.BUILDNET;
const privateKey = process.env.PRIVATE_KEY;
if (!privateKey) throw new Error("Missing PRIVATE_KEY in .env file");
const account = await WalletClient.getAccountFromSecretKey(privateKey);
if (!account.address) throw new Error("Missing address in account");
const client = await ClientFactory.createCustomClient(
  [
    { url: BUILDNET_URL, type: ProviderType.PUBLIC },
    { url: BUILDNET_URL, type: ProviderType.PRIVATE },
  ],
  BUILDNET_CHAIN_ID,
  true,
  account
);
const CHAIN_ID = ChainId.BUILDNET;
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
// user string input; in this case representing 20 USDC and 5 WMAS
const typedValueUSDC = "20";
const typedValueWMAS = "5";

// parse user input into decimal precision, which is 6 for USDC and 9 for WMAS
const tokenAmountUSDC = new TokenAmount(USDC, parseUnits(typedValueUSDC, USDC.decimals));
const tokenAmountWMAS = new TokenAmount(WMAS, parseUnits(typedValueWMAS, WMAS.decimals));

// set amount slipage tolerance
const allowedAmountSlippage = 50; // in bips, 0.5% in this case

// set price slippage tolerance
const allowedPriceSlippage = 50; // in bips, 0.5% in this case

// set deadline for the transaction
const currenTimeInMs = new Date().getTime();
const deadline = currenTimeInMs + 3_600_000;
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
const addLiquidityInput = pair.addLiquidityParameters(
  binStep,
  tokenAmountUSDC,
  tokenAmountWMAS,
  new Percent(BigInt(allowedAmountSlippage)),
  new Percent(BigInt(allowedPriceSlippage)),
  LiquidityDistribution.SPOT
);

const params = pair.liquidityCallParameters({
  ...addLiquidityInput,
  activeIdDesired: lbPairData.activeId,
  to: account.address,
  deadline,
});
```

## 6. Execute contractd call

```ts
// increase allowance for the router
const approveTxId1 = await new IERC20(USDC.address, client).approve(router, tokenAmountUSDC.raw);
const approveTxId2 = await new IERC20(WMAS.address, client).approve(router, tokenAmountWMAS.raw);

// add liquidity
const txId = await new IRouter(router, client).add(params);
console.log("txId", txId);
```
