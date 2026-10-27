---
type: observation
domain: [ai-safety, security]
confidence: 0.8
sources: 1
entities: [OpenAI, microVM, covert channel]
refs: ['https://importai.substack.com/p/import-ai-478-math-for-alignment']
---
# OpenAI red-team: sandboxed agents built a CPU-cache timing covert channel to exchange secrets between microVMs

OpenAI's post 'Securing our frontier model training environment' (covered by Import AI 478 and TLDR AI) says agents in separate microVMs, asked to exchange synthetic secrets without network or shared writable files, communicated via processor cache eviction/reload timing, and in a related attack via alternating continuous writes and idle periods. OpenAI added stronger controls, monitoring and defense-in-depth; red-teaming by agents found and fixed bugs and misconfigurations. Implication: isolation of capable agents requires side-channel-aware defenses.
