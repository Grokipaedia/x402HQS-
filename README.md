# x402HQS — High Quality Standards for x402 + IBA

**Safe Agentic Payments Stack**

x402 is the open payment rail (HTTP 402).  
IBA is the cryptographic authorization gate that makes agent payments safe and auditable.

### Neutral & Open Governance
x402HQS operates as a **vendor-agnostic resource hub**.  

As of April 2, 2026, the **x402 Foundation** officially launched under the **Linux Foundation**. The protocol was contributed by Coinbase with broad industry support from Cloudflare, Stripe, Google, AWS, Visa, Mastercard, Circle, Shopify, Solana Foundation, and others. This marks x402 as a neutral, community-governed standard for internet-native machine-to-machine payments.

We focus exclusively on the **authorization and audit layer** (IBA + WitnessBound) to prevent unauthorized drains, scope creep, and ensure compliance — the missing piece for safe agentic commerce.

### Core Layers
- **x402**: Instant stablecoin micropayments via HTTP  
- **IBA (Intent Bound Authorization)**: Signed intent certificates with hard bounds, payee lists, spend caps, and shard token delegation  
- **WitnessBound**: Immutable audit records

### Live Demos (HTML, no login required)
- Full x402 + IBA stack: https://x402hqs.com/x402-html/
- Shard token delegation: https://intentbound.com/shard-html/
- Additional examples: aipayhq.com/402-html/

### Repository Structure
- `iba-spec/` — Formal specification (intent certificates, bounds, shard tokens, WitnessBound)
- `demos/` — Source files for the live HTML demos
- `iba-sdk/` — Reference SDK placeholder (TypeScript/Python quickstarts coming in v0.1)

### Agent Quick-Start
Example IBA intent certificate (JSON structure agents can use):

```json
{
  "intentId": "iba-uuid-here",
  "humanSigner": "0xHumanWalletOrAgentOwner",
  "bounds": {
    "maxTotalSpend": "5.00",
    "asset": "USDC",
    "payees": ["0xAllowedPayeeAddress"],
    "scope": ["x402-payment", "api-access"],
    "expiresAt": "2026-05-01T00:00:00Z"
  },
  "shardDelegation": {
    "enabled": true,
    "maxDepth": 2
  }
}
