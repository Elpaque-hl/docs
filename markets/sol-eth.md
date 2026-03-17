# SOL/ETH — Trade the Solana Flippening

## Overview

SOL/ETH tracks the ratio of the SOL-PERP mark price to the ETH-PERP mark price, both native to Hyperliquid.

**Current ratio:** ~0.075 (SOL ≈ $140 / ETH ≈ $1,870)

## Specifications

| Parameter | Value |
|-----------|-------|
| Underlying | `markPrice(SOL) / markPrice(ETH)` |
| Contract multiplier | $100 |
| Max leverage | 10x |
| Initial margin | 10% |
| Oracle sources | Both Hyperliquid native |
| Funding | Hourly |

## Use cases

**The flippening trade.** SOL/ETH is the defining narrative of this cycle. Go long to bet Solana outperforms Ethereum; go short if you believe in the ETH comeback.

**Ecosystem rotation.** Capital rotates between L1 ecosystems. SOL/ETH captures this flow in a single instrument without absolute price exposure.

**Mean reversion.** The SOL/ETH ratio exhibits identifiable regimes and mean-reverting tendencies around macro events.

## Example

If you believe SOL will outperform ETH over the next month:

* **Long SOL/ETH** at 0.075 with 5x leverage
* If SOL/ETH moves to 0.080 → **+6.7% profit** (33.5% with leverage)
* If SOL/ETH drops to 0.070 → **-6.7% loss** (33.5% with leverage)

You profit regardless of whether both assets go up or down — only the ratio matters.
