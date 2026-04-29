# Same-Slot LUCID

Same-slot encrypted execution for Ethereum's LUCID encrypted mempool (EIP-8184).

Conditional commitments let builders decrypt and include protected transactions in the same slot — no extra latency, no compromises.

**Live:** [lucid-page-ashy.vercel.app](https://lucid-page-ashy.vercel.app)

**Proposal:** [ethresear.ch](https://ethresear.ch/t/same-slot-decryption-for-lucid-optional-n-execution-with-n-1-fallback/24576)

**EIP:** [EIP-8184: LUCID encrypted mempool](https://eips.ethereum.org/EIPS/eip-8184)

## Key Properties

- **Leaderless** — Block builders commit in parallel, no need to know the auction winner
- **Slot-time agnostic** — Works at 12s, 6s, or 3s slots without degradation
- **Incentive-complete** — Builders pay for keys, key publishers release because they're compensated
- **Zero user fee** — Builders bear the cost; users can set `key_publication_fee = 0`

## Deploy

Static HTML. Deploy to any hosting:

```bash
# Vercel
vercel deploy --prod

# Or just serve index.html
python3 -m http.server 8000
```

---

A contribution to the Encrypted Mempool initiative by [Primev](https://primev.xyz).
