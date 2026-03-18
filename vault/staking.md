# Staking

## Overview

Structured Perps is a decentralized exchange that requires 500,000 HYPE staked to a Hyperliquid validator to operate its HIP-3 markets. The spHYPE vault allows the community to participate in staking and earn real yield from the exchange's activity.

## How it works

1. **Deposit** HYPE into the vault
2. **Receive** spHYPE share tokens
3. **Earn** validator staking rewards + trading fee share
4. **Withdraw** anytime (subject to 500K minimum vault balance)

## spHYPE

* Non-rebasing — share price appreciates as revenue is distributed
* 1 spHYPE ≠ 1 HYPE — share price starts at 1.0 and increases over time

## Yield

spHYPE earns from two real revenue sources — not token emissions:

| Source | Description |
|--------|-------------|
| Validator staking | Native Hyperliquid staking yield (~2-3% APY) |
| Trading fee share | Portion of all trading fees generated on our exchange |

As trading volume grows, the fee share component scales proportionally.

## Withdrawals

* Permitted as long as vault balance stays above 500K HYPE
* Undelegation from validator takes ~24 hours
* Vault maintains a buffer above minimum for liquidity

## Smart contract

Deployed on HyperEVM (Chain ID 999). Community audit in progress.
