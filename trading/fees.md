# Fees & Funding

## Fees

Standard HIP-3 fee structure:

| Fee type | Rate |
|----------|------|
| Maker | 6 bps (0.06%) |
| Taker | 18 bps (0.18%) |

Fees are split 50/50 between the deployer and the Hyperliquid protocol.

## Funding rates

* **Frequency:** Hourly
* **Calculation:** Based on the deviation between mark price and oracle price
* **Direction:** Longs pay shorts when mark > oracle, and vice versa

## Revenue distribution

A portion of trading fees flows to spHYPE vault stakers. See [Staking](../vault/staking.md) for details.
