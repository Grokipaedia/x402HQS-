# x402HQS — High Quality Standards for x402 + IBA

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Patent Pending](https://img.shields.io/badge/Patent-Pending%20GB2603013.0-amber.svg)](https://intentbound.com)
[![NIST Filed](https://img.shields.io/badge/NIST-2025--0035%20Filed-green.svg)](https://intentbound.com/mandate-html/)

> **Safe Agentic Payments Stack. x402 is the rail. IBA is the gate.**

---

## The L3/L4 Architecture Gap

x402 solves the payment mechanics (L3). It creates a governance vacuum at L4.

An independent analysis published April 18, 2026 confirmed: *"By removing the friction of API keys, the protocol allows agents to spend freely — yet no open standard exists to decide if a transaction should be authorized."*

480,000 agents are now transacting on Agentic.Market (Coinbase, launched April 20, 2026) with no L4 authorization standard.

Mastercard built their own L4 layer — Verifiable Intent — announced March 5, 2026. The IBA patent was filed February 10, 2026. IBA predates Mastercard's framework by 23 days. The conception date is February 5, 2026, documented by OTS blockchain timestamp.

**x402HQS is the open, vendor-agnostic reference for the complete stack.**

---

## The Stack

| Layer | Protocol | Role |
|-------|----------|------|
| L3 · Payment | x402 · USDC · stablecoin rails | Payment mechanics · HTTP 402 |
| L4 · Authorization | IBA Intent Bound Authorization | What the agent is permitted to pay · to whom · up to what limit |
| L5 · Audit | WitnessBound | Immutable audit chain · every gate decision |

---

## Neutral & Open Governance

x402HQS operates as a **vendor-agnostic resource hub**.

As of April 2, 2026, the **x402 Foundation** officially launched under the **Linux Foundation** — contributed by Coinbase with backing from Cloudflare, Stripe, Google, AWS, Visa, Mastercard, Circle, Shopify, Solana Foundation, and others.

We focus exclusively on the **authorization and audit layer** (IBA + WitnessBound) — the missing piece for safe agentic commerce.

---

## Core Layers

- **x402**: Instant stablecoin micropayments via HTTP 402
- **IBA (Intent Bound Authorization)**: Signed intent certificates with hard bounds, payee lists, spend caps, financial limits, and shard token delegation
- **WitnessBound**: Immutable audit records

---

## Live Demos

- Full x402 + IBA stack: https://x402hqs.com/x402-html/
- Shard token delegation: https://intentbound.com/shard-html/
- Additional examples: aipayhq.com/402-html/

---

## Agent Quick-Start

Example IBA intent certificate for x402 payments:

```json
{
  "intentId": "iba-uuid-here",
  "humanSigner": "0xHumanWalletOrAgentOwner",
  "bounds": {
    "maxSinglePaymentUsd": "100.00",
    "maxSessionUsd": "1000.00",
    "asset": "USDC",
    "payees": ["0xAllowedMerchantAddress"],
    "scope": ["x402-payment", "api-access"],
    "expiresAt": "2026-12-31T00:00:00Z"
  },
  "defaultPosture": "DENY_ALL",
  "killThreshold": "drain_wallet | unauthorized_bulk_payment | sanctioned_address",
  "shardDelegation": {
    "enabled": true,
    "maxDepth": 2
  }
}
```

An agent that receives an x402 402 response from an undeclared merchant — BLOCK. The payment does not execute.

---

## Repository Structure

- `iba-spec/` — Formal specification (intent certificates, bounds, shard tokens, WitnessBound)
- `demos/` — Source files for the live HTML demos
- `iba-sdk/` — Reference SDK placeholder (TypeScript/Python quickstarts)

---

## Related Repos

| Repo | Track |
|------|-------|
| [iba-onchain-guard](https://github.com/Grokipaedia/iba-onchain-guard) | 6 onchain tracks · DeFi · wallet · x402 · DAO · NFT |
| [iba-governor](https://github.com/Grokipaedia/iba-governor) | Core gate · any agent |

---

## Patent & Standards Record

```
Patent:     GB2603013.0 (Pending) · UK IPO · Filed February 10, 2026
Conception: February 5, 2026 · OTS timestamp + witness email
            IBA predates Mastercard Verifiable Intent by 23 days (filing)
            and 28 days (conception)
WIPO DAS:   Confirmed April 15, 2026 · Access Code C9A6
PCT:        150+ countries · Protected until August 2028
IETF:       draft-williams-intent-token-00 · CONFIRMED LIVE
            datatracker.ietf.org/doc/draft-williams-intent-token/
NIST:       13 filings · NIST-2025-0035
NCCoE:      10 filings · AI Agent Identity & Authorization
```

---

## Acquisition Enquiries

IBA Intent Bound Authorization is available for acquisition.

**Jeffrey Williams**
IBA@intentbound.com
IntentBound.com · AgentialOnChain.com · x402HQS.com
Patent GB2603013.0 Pending · WIPO DAS C9A6 · IETF draft-williams-intent-token-00
