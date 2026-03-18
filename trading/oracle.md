# Oracle & Pricing

## Oracle

Each ratio perpetual has a dedicated oracle operated by Structured Perps, as required by the HIP-3 specification. The oracle computes:

```
ratio(t) = price(Asset A) / price(Asset B)
```

Prices are aggregated from multiple independent sources and submitted on-chain.

## Mark price

Mark price follows standard Hyperliquid mechanics and is used for margin calculations, liquidations, and unrealized P\&L.

## Funding rates

Funding rates follow standard Hyperliquid mechanics:

* **Frequency:** Hourly
* **Direction:** Longs pay shorts when mark price > oracle price (and vice versa)
