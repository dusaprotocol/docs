---
sidebar_position: 0
sidebar_label: Implement A Swap
---

# Implement A Swap

## Introduction

Swaps on Dusa can be executed through a router contract called `Router`. This contract will abstract some of the complexity of the swap, perform safety checks and will revert if certain conditions were to not be met. This is recommended way to use Dusa for most users.

The rest of the document describes:

- Which functions should be called to swap tokens
- How to use them in code examples

## Swap Functions

Swap functions can be broadly divided into two categories:

When the input amount is specified:

- `swapExactTokensForTokens`
- `swapExactTokensForMAS`
- `swapExactMASForTokens`

When the desired output amount is specified:

- `swapTokensForExactTokens`
- `swapTokensForExactMAS`
- `swapMASForExactTokens`

### When Input Amount Is Specified

- `swapExactTokensForTokens` - When you specify an exact amount of ERC-20 to swap for another ERC-20. E.g. USDC/DAI and you input USDC; router will then fetch how much DAI to expect as output and perform swap.
- `swapExactTokensForMAS` - When you specify an exact amount of ERC-20 to swap for MAS. E.g MAS/USDC and you input USDC; router will then fetch how much MAS to expect as output and perform swap.
- `swapExactMASForTokens` - When you specify an exact amount of MAS to swap for an ERC-20. E.g MAS/USDC and you input MAS; router will then fetch how much USDC to expect as output and perform swap.

### When Output Amount Is Specified

- `swapTokensForExactTokens` - When you specify exact amount of ERC-20 that you want to receive. E.g. USDC/DAI and you input USDC; router will then fetch how much DAI to transfer from your wallet and perform swap.
- `swapTokensForExactMAS` - When you specify exact amount of MAS that you want to receive. E.g. MAS/DAI and you input MAS; router will then fetch how much DAI to transfer from your wallet and perform swap.
- `swapMASForExactTokens` - When you specify exact amount of ERC-20 that you want to receive. E.g. MAS/DAI and you input DAI; router will then fetch how much MAS to transfer from your wallet and perform swap.

## Code Examples

#### 1. Swap 10 USDC for DAI using `swapExactTokensForTokens` with no intermediate swap paths:

```js
const amountIn = u256.from(u64(10**6));

USDC.increaseAllowance(router._origin, amountIn);

const tokenPath: IERC20[] = [USDC, DAI];
const pairBinSteps: u64[] = [1]; // pairBinSteps[i] refers to the bin step for the market (x, y) where tokenPath[i] = x and tokenPath[i+1] = y


const amountOut = router.getSwapOut(pair, amountIn, true).amountOut;
const amountOutWithSlippage: u256 = u256.div(u256.mul(amountOut, u256.from(99)), u256.from(100)) // We allow for 1% slippage
const masToSend: u64 = 10**8; // send 0.1 MAS for storage fee, surplus will be sent back at the end of the tx
const amountOutReal: u256 = router.swapExactTokensForTokens(amountIn, amountOutWithSlippage, pairBinSteps, tokenPath, receiverAddress, Context.timestamp(), masToSend);
```

#### 2. Swap 1 MAS for DAI using `swapExactMASForTokens` with no intermediate swap paths:

```js
let amountIn = u256.from(u64(10**9));

const tokenPath: IERC20[] = [WMAS, DAI];
const pairBinSteps: u64[] = [25]; 

const amountOut = router.getSwapOut(pairWMAS, amountIn, false).amountOut;
const amountOutWithSlippage = u256.div(u256.mul(amountOut, u256.from(99)), u256.from(100)) // We allow for 1% slippage
const masToSend: u64 = 10**8; // send 0.1 MAS for storage fee, surplus will be sent back at the end of the tx
amountIn += masToSend; // amountIn is the amount to swap & the storage Fee
const amountOutReal: u256 = router.swapExactMASForTokens(amountIn, amountOutWithSlippage, pairBinSteps, tokenPath, receiverAddress, Context.timestamp(), masToSend);
```

#### 3. Swap DAI to get 10 USDC output using `swapTokensForExactTokens` that routes through WMAS.

```js
const amountOut = u256.from(u64(10**6));
const amountInMax = u256.from(u64(11**6));

DAI.increaseAllowance(router._origin, amountInMax);

const tokenPath: IERC20[] = [DAI, WMAS, USDC];
const pairBinSteps: u64[] = [25, 20];
const masToSend: u64 = 10**8; // send 0.1 MAS for storage fee, surplus will be sent back at the end of the tx

// We define amountInMax as an arbitrary amount of 11e6 here
const amountsIn: u256 = router.swapTokensForExactTokens(amountOut, amountInMax, pairBinSteps, tokenPath, receiverAddress, Context.timestamp(), masToSend);
```
