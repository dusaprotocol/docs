---
sidebar_position: 9
sidebar_label: Limit Order
---
# Limit Order Hooks

## Overview

The Limit Order Hooks are sophisticated tools designed to facilitate advanced trading strategies by allowing users to automate orders at specified price levels. Traders can thus place buy (BID) or sell (ASK) orders at predetermined prices, maximizing profit potential while minimizing risk.

This implementation leverages the principle that concentrated liquidity positioned outside the current market price effectively functions as a limit order. When placing a limit order, users establish a one-sided liquidity position at their chosen bin price.

## Limitation

The fact that a limit order is a position implies some differences with existing off-chain solutions and different restrictions on its placement: 

Limit orders can only be placed at predefined bin prices within the selected liquidity pool.

Limit orders can only be placed above the token's price in a selected pool.

Limit orders cannot be placed exactly at the current active price (active ID).

All limit orders placed at the same bin price are aggregated into one position.

Users must manually trigger token retrieval after order execution by calling the `claim` method.

Orders are executed when their corresponding bin is crossed.

Limit orders do not expire automatically and must be manually canceled if no longer desired.

## How to Use Limit Order 

To add a limit order, users must first approve the token spending allowance to the contract, then call the `addLimitOrder` method, specifying the order type as `0` (selling tokenY) or `1` (selling tokenX), along with the token amount. Executing this call mints a one-sided liquidity position at the specified bin.

Limit orders execute automatically when the price within the liquidity pool moves entirely past or crosses through the order’s bin price. Each swap triggers the Limit Order Hooks, checking bin IDs to determine order execution. Once executed, the liquidity position is burned, and the resulting tokens are held by the Limit Order contract.

Existing orders can be increased in value by calling `editLimitOrder`. If the order hasn't been executed, it will add to the previous limit order; if it has and has not been claimed, it will claim the previous order and replace it with the new amount. The orderId will be the same.

After order execution, users must call the `claimOrder` method to retrieve their tokens. There is no expiration period for claims, and tokens remain secure in the contract indefinitely.

Users can manually cancel open limit orders at any time by calling the `cancelOrder` method. Note that if the pool price resides within the limit order's bin at cancellation time, the user receives tokens partially in both assets due to partial order execution.

Orders can be placed in native coins or tokens. If the input is in native coin, the function to create the order would be `addLimitOrderMas`, to edit it `editLimitOrderMas` and to cancel it `cancelOrderMas`. If the output is in native coin, the claim method is `claimOrderMas`. It is possible to still use the `cancelOrder` and `claimOrder` methods, the difference is that wrapped tokens will be received instead of native coins (WMAS instead of MAS).