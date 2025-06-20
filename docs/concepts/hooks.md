---
sidebar_class_name: hidden
sidebar_position: 7
sidebar_label: Hooks
---

# Hooks

## Introduction

Dusa V1.1 introduces Hooks — a system that lets developers customize and extend the behavior of liquidity pools.

## What is a Hook?

Hooks are external smart contracts that can be attached to individual pools to intercept and modify execution at key points during pool interactions.

They allow you to run custom logic before and/or after core operations like:
- new hook initialization
- Liquidity addition/removal
- Swaps
- LP token transfers
- Flashloans

Using hooks, developers can build advanced features such as:
- Custom AMMs with alternative pricing curves
- On-chain limit orders
- Yield farming mechanisms
- Custom oracle logic (e.g., median or truncated price feeds on top of [Dusa's Oracle](oracle.md#introduction))
- MEV-internalization strategies for LPs
- TWAMMs to split large orders over time

Each pool can be linked to a single hook. Hooks are optional, and developers can choose to implement only the functions they need.

Currently, only verified hooks can be added to the protocol. Each pool will indicate whether a hook is used and which one it is.
