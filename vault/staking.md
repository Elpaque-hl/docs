# Staking

## Overview

Structured Perps requires 500,000 HYPE staked to a Hyperliquid validator to operate HIP-3 markets. The svHYPE vault allows the community to pool HYPE toward this requirement and earn rewards.

## How it works

1. **Deposit** native HYPE into the vault
2. **Receive** svHYPE share tokens representing your ownership
3. **Earn** trading fee revenue + native staking rewards + points
4. **Withdraw** anytime (subject to the 500K minimum vault balance)

## svHYPE

svHYPE is the share token of the staking vault.

* **Non-transferable (soulbound)** — deposit and redeem only, no secondary market
* **Non-rebasing** — the share price appreciates as revenue is distributed
* **1 svHYPE ≠ 1 HYPE** — the share price starts at 1.0 and increases over time

When trading fees are deposited into the vault, the svHYPE share price increases proportionally for all holders.

## Revenue sources

| Source | Description |
|--------|-------------|
| Trading fee share | Portion of deployer revenue from all 3 markets |
| HL staking rewards | ~2.2% APY from native Hyperliquid validator staking |
| Points | Protocol points based on deposit size and duration |

## Withdrawals

* Withdrawals are permitted as long as the total vault balance stays above 500K HYPE
* Undelegation from the validator takes ~24 hours
* The vault maintains a buffer above the minimum to ensure liquidity

## Smart contract

The vault is deployed on HyperEVM (Chain ID 999). It accepts native HYPE directly — no WHYPE wrapping needed.

Key security features:
* ReentrancyGuard on all state-changing functions
* Owner-only admin functions
* On-chain event logging for all operations
* Community audit before launch
