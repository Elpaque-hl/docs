# Risks & FAQ

## Risks

### Oracle risk

* **Price feed failure** — Mitigated by circuit breakers that auto-pause markets
* **Price manipulation** — Hyperliquid mark prices use TWAP/EMA smoothing, resistant to single-trade manipulation
* **Stale prices** — 30-second staleness detection pauses quoting automatically

### Smart contract risk

The vault contract has not been formally audited. Community review is underway. Use at your own risk — never stake more than you can afford to lose.

### Liquidity risk

During the bootstrap phase, the protocol's market maker may be the primary liquidity provider. This limits order book depth. Spreads may be wider during low-activity periods.

### Staking risk

* **500K minimum** — Withdrawals may be temporarily restricted if vault balance is near the minimum
* **Undelegation delay** — 24 hours to undelegate from the validator
* **Slashing** — If protocol rules are violated, staked HYPE may be partially slashed

---

## FAQ

**What is a ratio perpetual?**

A perpetual contract that tracks `price(A) / price(B)` instead of a single asset price. It lets you trade the relative performance between two assets.

**Do I need HYPE to trade?**

No. Trading uses your USDC balance on Hyperliquid, like any other perpetual. You only need HYPE if you want to stake in the svHYPE vault.

**Can I trade on Hyperliquid directly?**

Yes. Our markets are standard HIP-3 perpetuals and appear on the Hyperliquid interface.

**What happens if both assets go down?**

You profit or lose based on the **ratio**, not absolute prices. If SOL drops 10% and ETH drops 15%, the SOL/ETH ratio went up — a long position profits.

**Are points worth anything?**

Points represent a commitment to early supporters. Their future utility will be announced as the protocol evolves.

**Is the smart contract audited?**

Community review is in progress. A formal audit is planned before mainnet launch.
