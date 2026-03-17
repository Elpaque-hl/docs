# Fees & Funding

## Fee schedule

Structured Perps uses the standard HIP-3 fee structure:

| Fee type | Rate |
|----------|------|
| Maker | 6 bps (0.06%) |
| Taker | 18 bps (0.18%) |

Fees are split 50/50 between the deployer (Structured Perps) and the Hyperliquid protocol.

## Growth Mode

During the early launch phase, Growth Mode may be activated — reducing or eliminating the deployer's fee share to attract initial trading volume. During Growth Mode, traders pay reduced fees while liquidity builds.

## Funding rates

Funding rates follow standard Hyperliquid mechanics:

* **Frequency:** Hourly
* **Calculation:** Based on the deviation between mark price and oracle price
* **Direction:** Longs pay shorts when the mark price is above oracle (and vice versa)

Funding rates for ratio perps tend to be lower than single-asset perps because the ratio is inherently less directional — both legs partially offset each other's funding exposure.

## Revenue distribution

A portion of trading fees is distributed to svHYPE vault stakers via share price appreciation. See [Staking](../vault/staking.md) for details.
