# Risks & FAQ

## Risks

### Oracle risk

Our custom oracle aggregates prices from multiple independent sources (CEXes + Hyperliquid). Risks include:

* **Price feed failure** — Mitigated by circuit breakers that auto-pause markets and multi-source validation that excludes outlier feeds
* **Price manipulation** — Multi-source aggregation makes single-exchange manipulation ineffective. Outlier detection discards deviating sources.
* **Stale prices** — 30-second staleness detection pauses quoting automatically

### Smart contract risk

The vault contract has not been formally audited. Community review is underway. Use at your own risk — never stake more than you can afford to lose.

### Liquidity risk

During the bootstrap phase, the protocol's market maker may be the primary liquidity provider. This limits order book depth. Spreads may be wider during low-activity periods.

### Staking risk

* **500K minimum** — Withdrawals may be temporarily restricted if vault balance is near the minimum
* **Undelegation delay** — 24 hours to undelegate from the validator
* **Slashing** — If protocol rules are violated (e.g. oracle misbehavior), staked HYPE may be partially slashed

---

## FAQ

**What is a ratio perpetual?**

A perpetual contract that tracks `price(A) / price(B)` instead of a single asset price. It lets you trade the relative performance between two assets in a single position.

**Why is this better than pair trading with two positions?**

With two separate positions, each leg has its own liquidation price based on the absolute price. If both assets pump, your short can get liquidated even if your thesis on relative performance is correct. With a ratio perp, liquidation is based on the ratio — you can't get liquidated when the ratio moves in your favor.

**Do I need HYPE to trade?**

No. Trading uses your USDC balance on Hyperliquid, like any other perpetual. You only need HYPE if you want to stake in the svHYPE vault.

**Can I trade on Hyperliquid directly?**

Yes. Our markets are standard HIP-3 perpetuals and appear on the Hyperliquid interface.

**What happens if both assets go down?**

You profit or lose based on the **ratio**, not absolute prices. If SOL drops 10% and ETH drops 15%, the SOL/ETH ratio went up — a long position profits.

**How does the oracle work?**

We operate our own custom oracle as required by HIP-3. It aggregates prices from multiple independent sources (centralized exchanges + Hyperliquid), cross-validates them, and submits the ratio price on-chain. See [Oracle & Pricing](../trading/oracle.md) for details.

**Are points worth anything?**

Points represent a commitment to early supporters. Their future utility will be announced as the protocol evolves.

**Is the smart contract audited?**

Community review is in progress. A formal audit is planned before mainnet launch.
