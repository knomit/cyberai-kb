---
type: observation
domain: [ai, agents, research]
confidence: 0.65
sources: 1
entities: []
motifs: [eval-set-overfitting]
refs: ['https://regularized-rsi.com/']
---
# RRSI proposes regularized recursive self-improvement for AI agent harnesses

The RRSI (Regularized Recursive Self-Improvement) method addresses agent harness self-improvement: an AI agent's capability is largely determined by its harness (prompts, control flow, configuration, context management, tools, skills, memory, sub-agents), and naively evolving the harness against a fixed evolve set causes it to memorize training tasks so large in-distribution gains shrink or vanish out of distribution. RRSI instead keeps the harness edit space open and regularizes the search trajectory through it, constraining how the search moves rather than what the harness may contain.
