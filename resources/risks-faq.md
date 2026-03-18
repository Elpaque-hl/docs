# Risks & FAQ

## Risks

### Smart contract risk

The vault contract has not been formally audited. Community review is underway. Use at your own risk.

### Liquidity risk

During early phases, spreads may be wider and order book depth limited.

### Staking risk

* Withdrawals may be restricted if vault balance is near the 500K minimum
* Undelegation delay: ~24 hours
* Slashing possible if protocol rules are violated

---

## FAQ

**What is a ratio perpetual?**

A perpetual contract that tracks `price(A) / price(B)`. Trade the relative performance between two assets in a single position.

**Why not just pair trade with two positions?**

Each leg has its own liquidation. If both assets pump, your short can get liquidated even when the ratio moves in your favor. Ratio perps solve this.

**Do I need HYPE to trade?**

No. Trading uses USDC on Hyperliquid. HYPE is only needed for staking.

**Can I trade on Hyperliquid directly?**

Yes. Our markets are standard HIP-3 perpetuals.

**What happens if both assets go down?**

You profit or lose based on the ratio. If HYPE drops 5% and ETH drops 15%, HYPE/ETH went up — a long profits.
