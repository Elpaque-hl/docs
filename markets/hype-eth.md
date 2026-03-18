# HYPE/ETH — Hyperliquid vs Legacy DeFi

## Overview

HYPE/ETH tracks the price ratio of HYPE to ETH, computed by our custom oracle aggregating prices from multiple independent sources.

**Current ratio:** ~0.0088 (HYPE ≈ $16.5 / ETH ≈ $1,870)

## Specifications

| Parameter | Value |
|-----------|-------|
| Underlying | `price(HYPE) / price(ETH)` |
| Contract multiplier | $100 |
| Max leverage | 10x |
| Initial margin | 10% |
| Oracle | Custom multi-source oracle (required by HIP-3) |
| Funding | Hourly |

## Use cases

**New vs Legacy DeFi.** HYPE represents the new wave — high-performance, community-first, revenue-generating. ETH represents the incumbent. HYPE/ETH captures this generational shift in a single instrument.

**Hyperliquid ecosystem conviction.** Rising HYPE/ETH signals capital flowing into the Hyperliquid ecosystem. The community can express their conviction without needing to short ETH separately and risk getting liquidated on it.

**ETH underperformance trade.** Go long HYPE/ETH if you believe Hyperliquid will continue to outperform legacy DeFi infrastructure, or short to fade it.

## Why HYPE/ETH and not two separate positions?

If you long HYPE and short ETH separately:
* ETH pumps 30% in a day → your short gets liquidated
* Even if HYPE pumped 50% → doesn't matter, the short leg already blew up

With HYPE/ETH ratio perps:
* HYPE/ETH ratio went from 0.0088 to ~0.0101 (+15%)
* You're in profit. No liquidation. One position, one risk.
