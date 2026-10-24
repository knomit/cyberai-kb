---
type: observation
domain: [security, supply-chain, ai]
confidence: 0.8
sources: 2
entities: [LiteLLM, GitHub, LiteLLM Agent Platform, PyPI]
motifs: [incomplete-secret-revocation]
refs: ['https://thehackernews.com/2026/10/leaked-litellm-master-key-let-attackers.html', 'kb://d88770a51516/kb/technology/security/supply-chain/litellm/1f37c7c5.md']
---
# LiteLLM unrevoked master key leaked in GitHub repo led to malicious package release

LiteLLM disclosed that on May 27, 2026 a config file committed to the public LiteLLM-Labs/lite-harness repository contained the master key of a LiteLLM Agent Platform deployment. The commit was force-pushed over and exposed keys flagged for revocation, but the master key was never revoked. An attacker used it on October 10, 2026 to access the Agent Platform and extract a GitHub CLI OAuth token, ultimately enabling a malicious version of the popular LiteLLM Python package to be pushed. Lesson: force-pushing over a leaked secret does not remove its validity; revocation must be verified. This is the root-cause disclosure for the compromised release recorded separately.
