# SOL/ETH — Solana vs Ethereum

## Overview

SOL/ETH tracks the price ratio of SOL to ETH, computed by our custom oracle aggregating prices from multiple independent sources.

**Current ratio:** ~0.075 (SOL ≈ $140 / ETH ≈ $1,870)

## Specifications

| Parameter | Value |
|-----------|-------|
| Underlying | `price(SOL) / price(ETH)` |
| Contract multiplier | $100 |
| Max leverage | 10x |
| Initial margin | 10% |
| Oracle | Custom multi-source oracle (required by HIP-3) |
| Funding | Hourly |

## Use cases

**L1 rotation.** Capital rotates between L1 ecosystems. SOL/ETH captures this flow in a single instrument without absolute price exposure.

**Relative value.** The SOL/ETH ratio exhibits identifiable regimes and mean-reverting tendencies around macro events. Trade the range without worrying about which way the broader market moves.

**No liquidation trap.** With a traditional pair trade (long SOL, short ETH), a broad market pump can liquidate your ETH short even if SOL outperforms. With SOL/ETH ratio perps, liquidation is based on the ratio — not individual prices.

## Example

If you believe SOL will outperform ETH over the next month:

* **Long SOL/ETH** at 0.075 with 5x leverage
* If SOL/ETH moves to 0.080 → **+6.7% profit** (33.5% with leverage)
* If SOL/ETH drops to 0.070 → **-6.7% loss** (33.5% with leverage)

You profit regardless of whether both assets go up or down — only the ratio matters.
