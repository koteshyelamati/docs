---
slug: /faq
sidebar_position: 99
title: FAQ
---

# Frequently Asked Questions

Quick answers to the questions newcomers ask most. For deeper detail follow the links to the relevant docs pages.

---

## How do I add Sentrix to MetaMask?

Open MetaMask → **Settings → Networks → Add a network** and fill in:

| Field | Mainnet | Testnet |
|---|---|---|
| **Network Name** | Sentrix Chain | Sentrix Testnet |
| **RPC URL** | `https://rpc.sentrixchain.com/rpc` | `https://testnet-rpc.sentrixchain.com/rpc` |
| **Chain ID** | `7119` | `7120` |
| **Currency Symbol** | `SRX` | `SRX` |
| **Block Explorer** | `https://scan.sentrixchain.com` | `https://scan-testnet.sentrixchain.com` |

Full walkthrough: [MetaMask Network Config](operations/metamask).

---

## Where can I get test SRX (testnet faucet)?

Use the testnet faucet linked from the [Developer Quickstart](operations/developer-quickstart). Connect your wallet to testnet (Chain ID `7120`) and request SRX — limits are per-address per day to prevent abuse.

---

## What are the mainnet and testnet Chain IDs?

| Network | Chain ID |
|---|---|
| Mainnet | `7119` |
| Testnet | `7120` |

Always double-check the Chain ID in your wallet to make sure you're on the right network.

---

## Where are the RPC, WebSocket, and REST endpoints?

Full reference: [API Endpoints](operations/api-endpoints) · [WebSocket Subscriptions](operations/websocket-subscriptions).

**Quick reference:**

| Protocol | Mainnet | Testnet |
|---|---|---|
| JSON-RPC / REST | `https://rpc.sentrixchain.com/rpc` | `https://testnet-rpc.sentrixchain.com/rpc` |
| WebSocket | `wss://rpc.sentrixchain.com/ws` | `wss://testnet-rpc.sentrixchain.com/ws` |

---

## How do I verify a smart contract?

After deploying, navigate to your contract on the [Sentrix Explorer](https://scan.sentrixchain.com), go to the **Contract** tab, and click **Verify & Publish**. Provide the source code, compiler version, and optimisation settings you used during deployment.

See the full guide in [Smart Contract Guide](operations/smart-contract-guide).

---

## How fast is block time and finality?

| | |
|---|---|
| **Block time** | ~1–2 seconds |
| **Finality** | Instant — Voyager DPoS+BFT achieves supermajority finality within the same block |

Unlike probabilistic finality chains, once a Sentrix block is committed it cannot be reverted under normal network conditions. You don't need to wait for confirmations.

---

## What is the total SRX supply and halving schedule?

- **Max supply:** 315 million SRX
- **Premine:** 20% of cap
- **Halving:** every 126 million blocks (~4 years), mirroring Bitcoin's schedule

Details: [Tokenomics Overview](tokenomics/overview) · [SRX](tokenomics/srx).

---

## Still have questions?

| Channel | Contact |
|---|---|
| Builder support | [builders@sentrixchain.com](mailto:builders@sentrixchain.com) |
| Validator support | [validators@sentrixchain.com](mailto:validators@sentrixchain.com) |
| GitHub Issues | [sentrix-labs/docs](https://github.com/sentrix-labs/docs/issues) |
