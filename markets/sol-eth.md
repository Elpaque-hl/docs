# SOL/ETH

Tracks the price ratio of SOL to ETH.

**Current ratio:** ~0.075

## Specifications

| Parameter | Value |
|-----------|-------|
| Underlying | `price(SOL) / price(ETH)` |
| Max leverage | 10x |
| Initial margin | 10% |
| Funding | Hourly |
| Settlement | USDC |

## Use cases

* **L1 rotation** — Trade SOL outperformance vs ETH without absolute price exposure
* **Relative value** — Mean-reverting behavior around macro events
* **Hedging** — Hedge ETH beta on a SOL long by going long SOL/ETH
