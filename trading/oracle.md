# Oracle & Pricing

## How prices work

Each ratio perpetual has a dedicated **custom oracle** operated by Structured Perps, as required by the HIP-3 specification. The oracle computes the ratio price in real time:

```
ratio(t) = price(Asset A) / price(Asset B)
```

Our oracle aggregates prices from multiple independent sources — including centralized exchanges (Binance, Bybit) and Hyperliquid's own mark prices — to compute a robust, manipulation-resistant ratio. The aggregated price is then submitted on-chain as the oracle price for each HIP-3 market.

**This is a requirement, not a choice.** HIP-3 mandates that each builder-deployed perpetual operates its own oracle. Relying solely on Hyperliquid's internal price feeds is not permitted and would result in slashing of the builder's stake.

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

### Multi-source validation

The oracle cross-checks prices across all sources before publishing. If any single source deviates significantly from the others, it is excluded from the aggregate. This protects against exchange-specific outages or manipulation.

## Market making

Liquidity is provided by an automated market maker based on the Avellaneda-Stoikov optimal quoting framework. The market maker:

* Quotes continuously on both sides with tight spreads (20-25 bps)
* Adjusts spreads dynamically based on real-time volatility
* Widens spreads when inventory is concentrated on one side
* Uses post-only (ALO) orders to ensure maker fee execution
* Refreshes quotes every 5 seconds
