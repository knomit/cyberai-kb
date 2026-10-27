---
type: observation
domain: [security, supply-chain, ai]
confidence: 0.8
sources: 1
entities: [LiteLLM, PyPI]
refs: ['https://thehackernews.com/2026/10/leaked-litellm-master-key-let-attackers.html']
---
# LiteLLM 1.107.0 malicious release: leaked Agent Platform master key enabled PyPI supply-chain attack

LiteLLM disclosed that a master key accidentally published to a public GitHub repo in late May 2026 let attackers push malicious LiteLLM 1.107.0. Its files auto-execute at Python startup even without importing LiteLLM, with a credential harvester (dev tools, AI apps, cloud, browsers) and a Unix backdoor fetching and running attacker code hourly. Treat leaked publishing keys as urgent; audit environments that installed 1.107.0.
