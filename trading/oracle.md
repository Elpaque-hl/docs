# Oracle & Pricing

## How prices work

Each ratio perpetual has a dedicated oracle that computes the ratio price in real time:

```
ratio(t) = markPrice(Asset A) / markPrice(Asset B)
```

Prices are sourced from Hyperliquid's WebSocket feed, which provides mark prices for all perpetual markets at sub-second granularity. **No third-party oracle dependency** — all underlying assets are native Hyperliquid perpetuals.

## Safety mechanisms

### Circuit breaker

If a ratio moves beyond a threshold within a 5-minute window, the oracle pauses and all market maker orders are cancelled. This prevents quoting during extreme volatility or potential manipulation events.

| Market | Threshold |
|--------|-----------|
| SOL/ETH | 6% in 5 minutes |
| HYPE/ETH | 8% in 5 minutes |
| ETH/BTC | 5% in 5 minutes |

HYPE/ETH has a wider threshold reflecting HYPE's higher natural volatility.

### Stale detection

If no price update is received for more than 30 seconds, the oracle pauses quoting until the feed resumes. This protects against stale prices during network issues.

## Market making

Liquidity is provided by an automated market maker based on the Avellaneda-Stoikov optimal quoting framework. The market maker:

* Quotes continuously on both sides with tight spreads (20-25 bps)
* Adjusts spreads dynamically based on real-time volatility
* Widens spreads when inventory is concentrated on one side
* Uses post-only (ALO) orders to ensure maker fee execution
* Refreshes quotes every 5 seconds
