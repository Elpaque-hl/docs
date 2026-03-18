# Staking

## Overview

Structured Perps requires 500,000 HYPE staked to a Hyperliquid validator to operate HIP-3 markets. The svHYPE vault allows the community to pool HYPE toward this requirement and earn rewards.

## How it works

1. **Deposit** HYPE into the vault
2. **Receive** svHYPE share tokens
3. **Earn** trading fee revenue + staking rewards + points
4. **Withdraw** anytime (subject to 500K minimum vault balance)

## svHYPE

* Non-rebasing — share price appreciates as revenue is distributed
* 1 svHYPE ≠ 1 HYPE — share price starts at 1.0 and increases over time

## Revenue sources

| Source | Description |
|--------|-------------|
| Trading fees | Portion of deployer revenue from all markets |
| Staking rewards | Native Hyperliquid validator staking yield |
| Points | Protocol points based on deposit size and duration |

## Withdrawals

* Permitted as long as vault balance stays above 500K HYPE
* Undelegation from validator takes ~24 hours
* Vault maintains a buffer above minimum for liquidity

## Smart contract

Deployed on HyperEVM (Chain ID 999). Community audit in progress.
