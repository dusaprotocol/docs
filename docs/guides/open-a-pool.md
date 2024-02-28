---
sidebar_position: 5
sidebar_label: Open a Pool
---

# Open a Pool

## Introduction

In this guide you can learn how to open a new liquidity pool on Dusa and to better understand the mechanisms behind it.

## Setting up a Pool

#### When creating a new pool it is important to consider:

1. The tokens that will be used in the pool
2. The bin step configuration
3. The inital active price

<p align="center">
  <img src="/img/open-a-pool.png" alt="Chart showing bin compositions" />
</p>

#### What's the difference between Base Assets and Quote Assets?

- Base Asset: This is the token that forms the basis of a trading pair. For example, if you're trading USDC/MAS, USDC would be the base asset. It's the token you're buying or selling.
- Quote Asset: This is the token used to price the base asset. In the USDC/MAS pair, MAS would be the quote asset. The price of the base asset is quoted in terms of the quote asset. So if USDC is priced at 10 MAS, it means you need 10 MAS to buy 1 USDC.

#### What is Bin Step and what is best for my pool?

In a Liquidity Pool, there are compartments known as "bins" that hold liquidity, with each bin representing a specific price point for the assets within the pool. These bins are combined to create a liquidity pool with a comprehensive price curve for the assets. Each bin is separated by a gap, which represents the price difference between them. This price difference is referred to as the "bin step".

#### What is the Initial Active Price?

The initial active price is the price at which the pool will start. It is important to set this price correctly as it will determine the initial position of the pool.

## Finalizing the Pool

After setting up the pool, you will need to execute the transaction to open it.
