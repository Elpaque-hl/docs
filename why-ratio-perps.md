# Why Ratio Perps?

## The problem with pair trading

To express a view like "HYPE will outperform ETH" on-chain today, you need to open two positions, manage two margins, and pay two sets of fees. Worse — **each leg has its own liquidation price based on the absolute price**.

If both assets pump and your thesis is correct (HYPE +60%, ETH +40%), your short ETH can still get liquidated — even though HYPE outperformed.

## The solution

A ratio perpetual collapses pair trading into a single position. Liquidation is based on the **ratio price**, not individual asset prices.

* One margin requirement
* One funding rate
* One fee
* One liquidation price — based on the ratio

You can't get liquidated when the ratio moves in your favor.

## Why Hyperliquid?

* **HIP-3** — Permissionless perp deployment with custom oracles
* **Sub-second finality** — HyperBFT consensus
* **Deep liquidity** — All underlying assets are native Hyperliquid perpetuals
* **HyperEVM** — Smart contract vaults on the same chain
