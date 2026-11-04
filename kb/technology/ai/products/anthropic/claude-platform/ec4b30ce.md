---
type: observation
domain: [ai, agents, api]
confidence: 0.8
sources: 2
entities: [Anthropic, Claude Platform, message threads]
motifs: [redundant-resend-elimination]
refs: ['https://claude.com/resources/articles/message-threads']
---
# Claude Platform message threads (public beta): send only new messages, ~35% lower median TTFT at 500K-1M tokens

Anthropic released message threads in public beta on the Claude Platform (early Nov 2026). Agents send only new messages instead of resending full conversation history. Per TLDR AI, it cut median time to first token by about 35% for requests of 500K-1M tokens, without changing token usage (i.e. a latency gain, not a cost reduction).
