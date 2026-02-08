# Hi, I'm Tchik Tchak

I build frontend applications that interact directly with smart contracts from the browser. No backend, no API keys, no framework — just vanilla JS, RPC nodes, and a lot of async debugging.


---

### What I work with

**Core frontend** — JavaScript (async/await, Promises, race conditions, ES modules), HTML/CSS (layout, animations, responsive — no framework), Vite, Git, Cloudflare Pages.

**Web3 integration** — ethers.js, @solana/web3.js, @bonfida/spl-name-service, ABI reading (ENS Registry, UNS, Name Wrapper), RPC multi-provider with fallback, Borsh serialization on Solana.

**The part that doesn't show in a stack list** — resilience engineering for unreliable networks: multi-RPC fallback, circuit breakers, retry with backoff, connection pre-warming, cache that never stores failures, race condition management between concurrent searches.

---

### Why this combination is unusual

Web3 frontend is a narrow niche. Most frontend developers don't deal with RPC nodes, on-chain data encoding, or the fact that a `null` response from a blockchain provider can mean five different things. Most blockchain developers don't think about skeleton loading, progressive feedback, or what happens when an ad-blocker interferes with an RPC call.

The real challenge isn't making each provider work individually — it's handling the cases where they silently fail (returning `null` instead of an error) while keeping response times acceptable for the user. Four providers, three blockchains, different failure modes, different response times, one search bar.

---

### What I've built

Coming SOON...

---

### Audit methodology

I audit my own code before shipping:

| Axe | Ce que je vérifie |
|---|---|
| **Reliability** | Retry, fallback, circuit breaker, cache — every failure path covered? |
| **Performance** | Time budget per resolution path, redundant RPC calls, timeout calibration |
| **Security** | XSS via malicious on-chain records, input validation, no client-side secrets, CSP |
| **Maintainability** | Coupling with third-party libs, technical debt of bypasses, error handling consistency |
| **Correctness** | Owner vs manager vs resolved address, stale cache, search race conditions |
| **Edge cases** | Expired domains, 100+ domain wallets, ad-blockers, empty records |
| **UX under constraint** | Progressive feedback during 3-10s RPC waits, skeleton loading, typed error states |
| **Observability** | Sentry breadcrumbs per resolution, error rates by provider, Discord user feedback |
| **Browser compat** | Ad-blocker interference with RPCs, neutral URL choices, no wallet extension dependency |

---

### What I'm not

I'm not a Solidity developer — I read contracts, I don't write them. I'm not a full-stack engineer — the constraints (bundle size, load time, lazy-loading blockchain SDKs on demand) led to vanilla JS, and it turned out to be the right call.

---

### Get in touch


[![Twitter](https://img.shields.io/badge/-Twitter-1DA1F2?style=flat&logo=twitter&logoColor=white)](https://twitter.com/TchikTchakX)
