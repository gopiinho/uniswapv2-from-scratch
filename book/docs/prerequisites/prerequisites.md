---
sidebar_position: 1
---

# Prerequisites

Before we continue building Uniswap V2, its better to have basic knowledge of few fundamentals. It is absolutely not necessary since we are going to cover some of these topics in incoming sections, it is still good to have prior muscle memory for these topics.


### DeFi Concepts

While I’ll explain all the core mechanisms, it helps to know:

- What a DEX (Decentralized Exchange) is
- What liquidity means
- The idea of swapping tokens without an order book

**Why**: Uniswap V2 is a [DEX](https://www.coinbase.com/en-in/learn/crypto-basics/what-is-a-dex) at its core, it allows swapping of tokens X and Y which are inside a token pair.


### Solidity

You should be comfortable reading and writing Solidity code - including concepts like:

- State variables, mappings, and structs
- Modifiers and events
- Interfaces and inheritance
  
**Why**: Uniswap V2 was written entirely written in Soldity ~0.5.0, since then the language has changed a lot but we will account for that and use the modern version to rewrite it.

### EVM Basics

A decent grasp on how the Ethereum Virtual Machine and transactions work:

- Gas, blocks, and transactions
- Contract addresses
- How `ERC20` tokens work and why `approve()`, and `transferFrom()` are used

**Why**: Swaps and liquidity provisions rely on tokens transfers and balance tracking.


### Mathematical Concepts

Just like me, you don't need to be a mathematician, but familiarity with:

- Understanding of constant product formula: `x * y = k`
- Multiplication & division of integers in Solidity
- Ratios and proportional reasoning

**Why**: Uniswap's pricing mechanisim depends entirely on these simple invariants.