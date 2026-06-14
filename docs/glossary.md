---
slug: /glossary
sidebar_position: 100
title: Glossary
---

# Glossary

Definitions for Sentrix-specific terms you'll encounter across the docs.

---

## BFT (Byzantine Fault Tolerance)

A property of a consensus algorithm that allows the network to reach agreement even if some nodes behave maliciously or fail. Sentrix's Voyager consensus uses a BFT supermajority (≥ 2/3 of stake) to finalise each block, making finality instant and irreversible.

## Block Time

The average interval between consecutive blocks. Sentrix targets **1 second** per block.

## DPoS (Delegated Proof of Stake)

A variant of Proof of Stake where token holders vote to elect a fixed set of validators who produce blocks on their behalf. Sentrix uses DPoS combined with BFT (see *Voyager DPoS+BFT*).

## Epoch

A fixed-length window of blocks after which validator sets and staking rewards are recalculated. At epoch boundaries, newly bonded validators become active and unbonding validators are removed.

## EVM (Ethereum Virtual Machine)

The bytecode execution environment shared across Ethereum and compatible chains. Sentrix is EVM-native, meaning Solidity/Vyper smart contracts and Ethereum tooling (Hardhat, Foundry, ethers.js, viem) work without modification.

## Finality

The point at which a transaction is guaranteed irreversible. Sentrix achieves **instant finality** — once a BFT supermajority signs a block, it cannot be reorganised.

## Halving

An event that cuts the block reward in half, mirroring Bitcoin's emission schedule. Sentrix halves every **126 million blocks** (~4 years).

## Jail / Unjail

When a validator misses too many blocks or double-signs, it is *jailed*: removed from the active set and its stake slashed. A jailed validator must submit an *unjail* transaction (after a cooldown period) to re-enter the active set.

## libp2p

A modular peer-to-peer networking library used by Sentrix for node discovery and gossip. Provides transport-agnostic connections between chain nodes.

## MDBX

A high-performance embedded key-value database used by Sentrix to store chain state. Chosen for its ACID guarantees, memory-mapped I/O, and compaction behaviour.

## Precommit / Prevote

Phases in the Voyager BFT round:
- **Prevote** — validators broadcast a vote for the block proposed in this round.
- **Precommit** — after a supermajority of prevotes, validators broadcast a precommit. A supermajority of precommits finalises the block.

## revm

The Rust-native EVM implementation used by Sentrix for transaction execution. Chosen for safety (Rust ownership model) and throughput.

## SRX / sentri

**SRX** is the native token of Sentrix Chain. *Sentri* is an informal nickname. SRX is used for gas fees, staking, and governance.

- **Max supply:** 315 million SRX
- **Premine:** 20% of cap

## Staking

Locking SRX with a validator to participate in block production and earn staking rewards. Staked SRX is subject to a *slashing* penalty if the validator misbehaves.

## Validator / Full Node

- **Validator** — a staked node that participates in consensus: proposes and votes on blocks. Requires a minimum stake bond.
- **Full Node** — a node that follows the chain and executes all transactions but does not participate in consensus (no stake required).

## Voyager DPoS+BFT

The name of Sentrix's consensus protocol. It combines Delegated Proof of Stake (validator election by token holders) with a BFT finalisation layer (supermajority vote per block), achieving 1-second blocks and instant finality. Live since April 2026.

---

*See also: [Architecture Overview](architecture/overview) · [Staking](tokenomics/staking) · [Validator Guide](operations/validator-guide)*
