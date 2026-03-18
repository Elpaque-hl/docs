# Why Ratio Perps?

## The problem

Pair trading is one of the oldest strategies in finance. But on-chain, expressing a view like "HYPE will outperform SOL" requires:

1. Opening a long position on HYPE
2. Opening a short position on SOL
3. Continuously rebalancing both legs
4. Managing margin and liquidation risk on **two separate positions**
5. Paying fees on both legs

And here's the critical issue — **you can get liquidated even when your thesis is correct.**

## The liquidation trap

Imagine you believe HYPE will outperform SOL. You go long HYPE and short SOL. Both assets pump — HYPE goes up 60% and SOL goes up 40%. Your thesis was right: HYPE outperformed SOL by 20%.

But your **short SOL position just moved 40% against you**. With 5x leverage, that's a 200% loss on the short leg. You get liquidated on the SOL short — even though you were right about the relative performance.

This is the fundamental flaw of pair trading with two separate positions: **each leg has its own liquidation price based on the absolute price**, not the relative performance between the two assets.

## The solution

A ratio perpetual collapses this into **a single position** where liquidation is based on the **ratio price**, not the individual asset prices.

* One margin requirement
* One funding rate
* One fee
* **One liquidation price — based on the ratio, not absolute prices**

In the example above, HYPE/SOL went from 1.0 to ~1.14 (+14%). With a ratio perp at 5x leverage, that's a +70% profit. No liquidation risk from both assets pumping — because the ratio moved in your favor.

**You can't get liquidated when your directional thesis on the ratio is correct.** That's the whole point.

## Who is this for?

**Pair traders.** Express views like "HYPE will outperform SOL" or "ETH will outperform BTC" in a single instrument instead of managing two legs with independent liquidation risk.

**Hedgers.** A trader long SOL-PERP can hedge ETH beta by going long SOL/ETH — capturing SOL alpha without absolute price exposure.

**Relative value traders.** The ratio between two assets is inherently less volatile than either asset alone. This means tighter spreads, lower funding, and more predictable risk.

## Why Hyperliquid?

Hyperliquid is the only venue where this product is possible today:

* **HIP-3** enables permissionless perp deployment with custom oracles
* **Sub-second block times** on HyperBFT consensus
* **Deep liquidity** on all underlying assets (SOL, ETH, BTC, HYPE are all native)
* **HyperEVM** for smart contract vaults and revenue distribution
* **Unified API** — same interface for all perpetuals regardless of deployer

No other chain has the combination of speed, liquidity, and permissionless deployment needed for ratio perpetuals.
