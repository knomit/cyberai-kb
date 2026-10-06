---
type: observation
domain: [security, hardware]
confidence: 0.8
sources: 1
entities: [Spectre v2, Intel, Branch Target Reuse, Spectre-v2 BTR, VUSec, GraalVM, SpiderMonkey, Linux kernel]
refs: ['https://thehackernews.com/2026/09/new-spectre-v2-btr-attack-leaks-linux.html', 'https://www.vusec.net/projects/btr']
---
# Spectre v2 Branch Target Reuse (BTR) leaks Linux root password hash on Intel in 3-5 minutes

BTR, a Spectre v2 variant, exploits stale branch-predictor state after a JIT engine reuses memory; researchers leaked a root password hash on Raptor Cove and Lion Cove in about 3 and 5 minutes on average. No current CPU has a mechanism to resync predictor and code state.
