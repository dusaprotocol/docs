---
sidebar_position: 0
sidebar_label: Introduction
---

# Introduction

SDK is an open source library created to help builders interact with the contracts from their JS/TS projects.

This guide endeavors to show examples of how builders can use the SDK, together with [massa-web3](https://github.com/massalabs/massa-web3), to perform a trade, add/remove liquidity, and claim fees.

## Installation

Run the following command to add the required dependencies to your project:

```shell
npm install @dusalabs/sdk @massalabs/massa-web3
```


## Classes
SDK implements 4 main classes: `PairV2`, `RouteV2`, `TradeV2`, and `Bin`. Specific documentation of the fields and functions for each class can be found in the code.

* [PairV2](https://github.com/dusaprotocol/sdk/blob/main/src/v2entities/pair.ts)
* [RouteV2](https://github.com/dusaprotocol/sdk/blob/main/src/v2entities/route.ts)
* [TradeV2](https://github.com/dusaprotocol/sdk/blob/main/src/v2entities/trade.ts)
* [Bin](https://github.com/dusaprotocol/sdk/blob/main/src/v2entities/bin.ts)

## Github
SDK uses Github to track issues and feature requests. Please open an issue if you have found a bug or have new feature requests. We also welcome contributions from the open source community. Open a pull request with a detailed explanation and the team will gladly review your contribution.

| Repo | Github URL |  NPM URL |
| :-------: | :----: | :----: |
| V2 | https://github.com/dusaprotocol/sdk |  https://www.npmjs.com/package/@dusalabs/sdk |
