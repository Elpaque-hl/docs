# Welcome

**The first on-chain ratio perpetuals exchange.**

Structured Perps brings ratio perpetual contracts to Hyperliquid via HIP-3. Trade the relative performance between two assets in a single position.

## Why ratio perps?

A ratio perp tracks `price(A) / price(B)`. Instead of managing two separate positions to pair trade, you get:

* **Single position** — One margin, one liquidation price, one fee
* **No liquidation trap** — Liquidation is based on the ratio, not individual asset prices
* **Up to 10x leverage** — Capital-efficient exposure to relative value
* **24/7 trading** — Crypto-native assets, markets never close

## Markets

| Market | Ratio | Description |
|--------|-------|-------------|
| **SOL/ETH** | ~0.075 | Solana vs Ethereum |
| **HYPE/ETH** | ~0.0088 | Hyperliquid vs legacy DeFi |
| **ETH/BTC** | ~0.028 | The classic macro rotation |

All markets are standard HIP-3 perpetuals on Hyperliquid with hourly funding.

{% content-ref url="trading/getting-started.md" %}
[getting-started.md](trading/getting-started.md)
{% endcontent-ref %}

{% content-ref url="vault/staking.md" %}
[staking.md](vault/staking.md)
{% endcontent-ref %}
