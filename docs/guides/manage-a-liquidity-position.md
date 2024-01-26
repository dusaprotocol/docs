---
sidebar_position: 1
sidebar_label: Manage A Liquidity Position
---

# Manage A Liquidity Position

## Introduction

Managing liquidity on Dusa can be executed through a router contract called `Router`. This contract will abstract some of the complexity of the liquidity management, perform safety checks and will revert if certain conditions were to not be met. This is recommended way to use Dusa for most users.

Liquidity can be concentrated in arbitrary shapes and any price range the user desires.

Next sections explain how to:

- How are new pairs created
- How to add liquidity
- How to remove liquidity

## Pair Creation

Creating new pools is **not currently permissionless**. However, this can be switched on by the protocol owner via the boolean `creationUnlocked()` in the `Factory` contract.

To create a new pair, the `createLBPair` function of the `Factory` contract is called.

```js
function createLBPair(
    tokenX: Address,
    tokenY: Address,
    activeId: u32,
    binStep: u32,
  ): Address {};
```

The pair creator sets the initial price via the `activeId` argument.

It is important to note that there can be multiple markets of the same pair, but only differing in their bin step.

Pools are therefore uniquely identified by the tuple `(tokenX, tokenY, binStep)`.

After pair creation tokens can be added to any desired bin provided that:

- Above bin `activeId` only `tokenX` can be added
- Below bin `activeId` only `tokenY` can be added
- Both `tokenX` and `tokenY` liquidity can be added to bin `activeId`

## Adding Liquidity

To add liquidity, the `LiquidityParameters` class is as input:

```js
function addLiquidity(liquidityParameters: LiquidityParameters): AddLiquidity {};

function addLiquidityMAS(liquidityParameters: LiquidityParameters): AddLiquidity {};

```

### Liquidity Parameters

```js
class LiquidityParameters {
  /**
   * @param {IERC20} tokenX - Has to be the same as tokenX defined in Pair contract
   * @param {IERC20} tokenY - Has to be the same as tokenY defined in Pair contract
   * @param {u64} binStep - // Has to point to existing pair
   * @param {u256} amountX - The amount to send of token X
   * @param {u256} amountY - The amount to send of token Y
   * @param {u256} amountXMin - The min amount of token X added to liquidity
   * @param {u256} amountYMin - The min amount of token Y added to liquidity
   * @param {u64} activeIdDesired - The active id that user wants to add liquidity from
   * @param {u64} idSlippage - The number of id that are allowed to slip
   * @param {Array<i64>} deltaIds - The list of delta ids to add liquidity (`deltaId = activeId - desiredId`)
   * @param {Array<u256>} distributionX - The distribution of tokenX with sum(distributionX) = 1e18 (100%) or 0 (0%)
   * @param {Array<u256>} distributionY - The distribution of tokenY with sum(distributionY) = 1e18 (100%) or 0 (0%)
   * @param {Address} to - The address of the recipient
   * @param {u64} deadline - Block timestamp cannot be lower than deadline
   */
  constructor(
    public tokenX: IERC20 = new IERC20(new Address('')),
    public tokenY: IERC20 = new IERC20(new Address('')),
    public binStep: u64 = 0,
    public amountX: u256 = u256.Zero,
    public amountY: u256 = u256.Zero,
    public amountXMin: u256 = u256.Zero,
    public amountYMin: u256 = u256.Zero,
    public activeIdDesired: u64 = 0,
    public idSlippage: u64 = 0,
    public deltaIds: Array<i64> = [],
    public distributionX: Array<u256> = [],
    public distributionY: Array<u256> = [],
    public to: Address = new Address(''),
    public deadline: u64 = 0,
  ) {}
}
```

The number of parameters are quite extensive. Here are a few pointers to understand how to construct them better:

- The active bin ID may change from the time you decided to add liquidity to when it is actually added. Therefore, you define `activeIdDesired` and `idSlippage` to account for when the price moves.
- `deltaIds` define which bins liquidity will be added to relative to `activeId`, 0 being the active bin. All positive values are bins with only X and all negative values are bins with only Y.
- `distributionX` (or `distributionY`) is the percentages of `amountX` (or `amountY`) you want to add to each bin.
  - Sum of all values should be less than or equal to 1. If less than, the remaining is refunded back to the user. With values going from 0 (0%) to 1e18 (100%).
  - Trying to add X to a bin below the active bin or Y to a bin above the active bin will cause a revert.
- Maximum number of bins, that can be populated at the same time is around `50` on Massa due to block gas limit. Multiple transactions can be used to add liquidity to more bins.

### Code Example

In this example, we add 100 USDC and 100 USDT into three bins: active bin, bin below and bin above.

We define the distributions as follow:

- For asset X (USDC), we add 50 USDC to the active bin and 50 USDC to the bin above.
- For asset Y (USDT), we add 33.3 USDT to the active bin and 66.6 USDT to the bin below.

We also allow a bin ID slippage of 5 just in case bin moves in the time it takes to execute the transaction.

```js
const PRECISION: u256 = u256.from(u64(10 ** 18));
const binStep: u32 = 25;
const amountX = u256.mul(u256.from(100), u256.from(u64(10 ** 6)));
const amountY = u256.mul(u256.from(100), u256.from(u64(10 ** 6)));
const amountXmin = u256.mul(u256.from(99), u256.from(u64(10 ** 6))); // We allow 1% amount slippage
const amountYmin = u256.mul(u256.from(99), u256.from(u64(10 ** 6))); // We allow 1% amount slippage

const activeIdDesired: u64 = 2**23; // We get the ID from price using getIdFromPrice()
const idSlippage: u64 = 5;

const deltaIds: i64[] = [-1, 0, 1];
const distributionX: u256[] = [u256.Zero, u256.div(PRECISION, u256.from(2)), u256.div(PRECISION, u256.from(2))];
const distributionY: u256[] = [u256.div(u256.mul(u256.from(2), PRECISION), u256.from(3)), u256.div(PRECISION, u256.from(3)), u256.Zero];


const liquidityParameters = new LiquidityParameters(
    USDC,
    USDT,
    binStep,
    amountX,
    amountY,
    amountXmin,
    amountYmin,
    activeIdDesired,
    idSlippage,
    deltaIds,
    distributionX,
    distributionY,
    receiverAddress,
    Context.timestamp()
);

USDC.increaseAllowance(router._origin, amountX);
USDT.increaseAllowance(router._origin, amountY);

const AddLiquidityReturn = router.addLiquidity(liquidityParameters);
const liquidityMinted: u256[] = AddLiquidityReturn.liquidityMinted;
const depositIds: u64[] = AddLiquidityReturn.depositIds;

```

## Removing Liquidity

There are some key differences between adding and removing liquidity:

1. We don't use the `LiquidityParameters` struct.
2. We use absolute bin IDs instead of relative bin IDs.
3. Because we use absolute bin IDs, bin slippage is not possible.
4. We define absolute `LBToken` balances to remove from each bin.
   - In bins below active bin, balances consist of only Y.
   - In bins above active bin, balances consist of only X.
   - In the active bin, the balance consists of a share of X and Y.

To remove liquidity, we use one of the router functions below:

```js
function removeLiquidity(
    tokenX: Address,
    tokenY: Address,
    binStep: u32, // Has to point to existing pair that user has liquidity deposited in
    amountXMin: u256, // Minimum amount of token X that has to be withdrawn
    amountYMin: u256, // Minimum amount of token Y that has to be withdra
    ids: Array<u64>, // Bin IDs that liquidity should be removed from
    amounts: Array<u256>, // LBToken amount that should be removed
    to: Address, // Receiver address
    deadline: u64, // Block timestamp cannot be lower than deadline
  ): Amounts {};

function removeLiquidityMAS(
    token: Address,
    binStep: u32,
    amountTokenMin: u256,
    amountMasMin: u256,
    ids: Array<u64>,
    amounts: Array<u256>,
    to: Address,
    deadline: u64,
  ): Amounts {};
```

Here are some pointer for using these functions:

1. Lengths of `ids` and `amounts` must be the same.
2. Values in `amounts` are `LBToken` amounts.
3. Maximum number of bins that can be withdrawn at the same time is around `40` due to Massa block gas limit. In this case, multiple transactions can be used to remove more liquidity.

### Code Example

```js
const numberOfBinsToWithdraw: i32 = 3;
const binStep: u32 = 25;

let amounts: u256[] = [u256.Zero, u256.Zero, u256.Zero];
const ids: u64[] = [8388605, 8388608, 8388611];

let totalXBalanceWithdrawn = u256.Zero;
let totalYBalanceWithdrawn = u256.Zero;

// To figure out amountXMin and amountYMin, we calculate how much X and Y underlying we have as liquidity
for (let i = 0; i < numberOfBinsToWithdraw; i++) {
    const LBTokenAmount: u256 = pair.balanceOf(receiverAddress, ids[i]);
    amounts[i] = LBTokenAmount;
    const bin = pair.getBin(u32(ids[i]));

    totalXBalanceWithdrawn = u256.add(totalXBalanceWithdrawn, u256.div(u256.mul(LBTokenAmount, bin.reserveX), pair.totalSupply(ids[i])));
    totalYBalanceWithdrawn = u256.add(totalYBalanceWithdrawn, u256.div(u256.mul(LBTokenAmount, bin.reserveY), pair.totalSupply(ids[i])));
}

const amountXMin: u256 = u256.div(u256.mul(totalXBalanceWithdrawn, u256.from(99)), u256.from(100)); // Allow 1% slippage
const amountYMin: u256 = u256.div(u256.mul(totalYBalanceWithdrawn, u256.from(99)), u256.from(100)); // Allow 1% slippage

pair.setApprovalForAll(true, router._origin);

const returnAmounts = router.removeLiquidity(
    USDC._origin,
    WMAS._origin,
    binStep,
    amountXMin,
    amountYMin,
    ids,
    amounts,
    receiverAddress,
    Context.timestamp()
);
const amountXWithdrawn = returnAmounts.amountX;
const amountYWithdrawn = returnAmounts.amountY;
```
