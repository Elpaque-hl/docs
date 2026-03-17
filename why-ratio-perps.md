# Why Ratio Perps?

## The problem

Pair trading is one of the oldest strategies in finance. But on-chain, expressing a view like "SOL will outperform ETH" requires:

1. Opening a long position on SOL
2. Opening a short position on ETH
3. Continuously rebalancing both legs
4. Managing margin and liquidation risk on **two separate positions**
5. Paying fees on both legs

## The solution

A ratio perpetual collapses this into **a single position** with:

* One margin requirement
* One funding rate
* One fee
* One liquidation price

The economic equivalence is exact — but the execution is dramatically simpler and more capital efficient.

## Who is this for?

**Pair traders.** Express views like "SOL will outperform ETH" or "HYPE will outperform ETH" in a single instrument instead of managing two legs.

**Hedgers.** A trader long SOL-PERP can hedge ETH beta by going long SOL/ETH — capturing SOL alpha without absolute price exposure.

**Narrative traders.** Ratio instruments create viral, narrative-driven markets. SOL/ETH captures the "Solana flippening." HYPE/ETH captures "new DeFi vs old DeFi." Everyone has an opinion.

## Why Hyperliquid?

Hyperliquid is the only venue where this product is possible today:

* **HIP-3** enables permissionless perp deployment with custom oracles
* **Sub-second block times** on HyperBFT consensus
* **Deep liquidity** on all underlying assets (SOL, ETH, BTC, HYPE are all native)
* **HyperEVM** for smart contract vaults and revenue distribution
* **Unified API** — same interface for all perpetuals regardless of deployer

No other chain has the combination of speed, liquidity, and permissionless deployment needed for ratio perpetuals.
