# ETH/BTC — The Classic Macro Ratio

## Overview

ETH/BTC tracks the price ratio of ETH to BTC, computed by our custom oracle aggregating prices from multiple independent sources.

**Current ratio:** ~0.028 (ETH ≈ $1,870 / BTC ≈ $67,000)

## Specifications

| Parameter | Value |
|-----------|-------|
| Underlying | `price(ETH) / price(BTC)` |
| Contract multiplier | $100 |
| Max leverage | 10x |
| Initial margin | 10% |
| Oracle | Custom multi-source oracle (required by HIP-3) |
| Funding | Hourly |

## Use cases

**ETH/BTC ratio trading.** The most watched ratio in crypto. Every macro trader monitors ETH/BTC. Go long if you believe ETH will outperform BTC; short if BTC dominance continues to rise.

**Cross-asset hedging.** A trader long ETH-PERP can short ETH/BTC to isolate ETH alpha from BTC beta — hedging broad market risk while retaining ETH-specific exposure.

**Institutional-grade pair trading.** ETH/BTC is a staple of traditional crypto fund strategies. With ratio perps, no need to manage two legs — one position, one margin, one liquidation based on the ratio.
