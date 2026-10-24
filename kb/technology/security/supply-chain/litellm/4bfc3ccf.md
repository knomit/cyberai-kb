---
type: observation
domain: [security, supply-chain, ai]
confidence: 0.8
sources: 1
entities: [LiteLLM, GitHub, PyPI]
motifs: [incomplete-secret-revocation]
refs: ['https://thehackernews.com/2026/10/leaked-litellm-master-key-let-attackers.html']
---
# Root cause of LiteLLM compromise: unrevoked Agent Platform master key leaked May 2026

LiteLLM disclosed that on May 27, 2026 a config file committed to the public LiteLLM-Labs/lite-harness repo contained the master key of a LiteLLM Agent Platform deployment. The commit was force-pushed over and keys flagged for revocation, but the master key was never revoked. An unknown attacker (from 69.48.229[.]143) used it on October 10, 2026 to access the Agent Platform and extract a GitHub CLI OAuth token, ultimately allowing a malicious version of the popular LiteLLM Python package to be pushed. Lesson: force-pushing over a commit does not neutralize a leaked secret; revocation must be verified. Reported by The Hacker News 2026-10-24.
