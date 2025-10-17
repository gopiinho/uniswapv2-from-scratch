---
sidebar_position: 2
---

# Uniswap V2 Architecture

Uniswap V2 at its core is very simple, it has 3 core contracts, [**`UniswapV2Pair`**](https://github.com/Uniswap/v2-core/blob/master/contracts/UniswapV2Pair.sol), [**`UniswapV2Factory`**](https://github.com/Uniswap/v2-core/blob/master/contracts/UniswapV2Factory.sol), and [**`UniswapV2Router02`**](https://github.com/Uniswap/v2-periphery/blob/master/contracts/UniswapV2Router02.sol). And before we continue on building them from scratch it would make sense to get a brief overview on what role each of these contracts serve to whole protocol. 

### UniswapV2Pair

Possibly the most important contract to discuss in this section, **UniswapV2Pair** at its core is a contract that holds a pair of ERC20 tokens that traders can swap against or liquidity providers can provide liquidity for. Every single pair of tokens uses seperate UniswapV2Pair contract to manage it. 

**UniswapV2Pair** is also an ERC20 token, so it uses this token to keep track of liquidity share ownership of lp providers, similar to how [ERC4626](https://rareskills.io/post/erc4626) operate. 

If desired **UniswapV2Pair** contract does not exist then you can create a new one with **UniswapV2Factory** contract.

### UniswapV2Factory

As its name suggests, it a factory contract that let's you create a new **UniswapV2Pair** for two ERC20 tokens, hence allowing lp providers to add liqidity for those tokens enabling traders to swap between those tokens.

### UniswapV2Router02

Secound version of their router contract, it is user by traders, developers or other smart contracts to interact with the **pair** contracts instead of directly interacting with them, as it is the recommended way to do so.

---

And, that is it, these are the three main smart counts that make up the Uniswap V2 as we know it as. The whole architecture is fairly simple yet powerful and that is the reason why it has stood the test of time.