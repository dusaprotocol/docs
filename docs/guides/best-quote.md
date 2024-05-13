---
sidebar_position: 2
sidebar_label: Finding The Best Quote
---

# Finding The Best Quote

## Introduction

Finding the optimal quote for a givien tokens path can be obtained through the `Quoter` contract. This contract will find the best combinations of swaps accross pairs in order to optimise cost.

The rest of the document describes:

- Which functions to call to get the optimal quote from an input and output amount.
- Code examples that illustrate use cases. 

## Find The Best Quote From Amount In

This function retrieves the best route of swaps for a given input amount.

```js
function findBestPathFromAmountIn(route: address[], amountIn: u256): Quote {}
```

The output of this function is quite substantial. Here are the specifications to understand it better:

```js
class Quote {
  /**
   *
   * @param {Address[]} route Path in the form of an array of token address to go through
   * @param {Address[]} pairs Address of the different pairs to do through
   * @param {u64[]} binSteps Bin step for each pair
   * @param {u256[]} amounts The amounts for every step of the swap
   * @param {u256[]} virtualAmountsWithoutSlippage The virtual amounts of every step of the swap without slippage
   * @param {u256[]} fees The fees to pay for every step of the swap
   */
  constructor(
    public route: Address[] = [],
    public pairs: Address[] = [],
    public binSteps: u64[] = [],
    public amounts: u256[] = [],
    public virtualAmountsWithoutSlippage: u256[] = [],
    public fees: u256[] = [],
  ) {}
}
```
### Code Example

In this example, we want to swap 10 USDC to DAI. A possible route is to go through the WMAS route in between:

```js
const tokenPath: address[] = [USDC, WMAS, DAI];

const amountIn = u256.from(u64(10 * 10**6));

const quote = quoter.findBestPathFromAmountIn(tokenPath, amountIn);
```

## Find The Best Quote From Amount Out

This function retrieves the best route of swaps for a given output amount.

```js
function findBestPathFromAmountOut(route: Address[], amountOut: u256): Quote {}
```

### Code Example

In this example, we want to own 10 USDC and we would like to know how many DAI is required to perform the if we want to go through the WMAS route:
```js
const tokenPath: address[] = [USDC, WMAS, DAI];

const amountOut = u256.from(u64(10 * 10**6));

const quote = quoter.findBestPathFromAmountOut(tokenPath, amountOut);
```