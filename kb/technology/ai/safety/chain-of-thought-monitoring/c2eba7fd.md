---
type: concept
domain: [ai, safety, interpretability, oversight]
confidence: 0.8
sources: 2
entities: [Redwood Research, GPT-6 Astra]
motifs: [monitorability-erosion, architecture-undermines-oversight]
refs: ['https://blog.redwoodresearch.org/p/an-operationalization-of-opaque-serial', 'kb://d88770a51516/kb/technology/ai/architecture/transformer-variants/57200a89.md']
---
# Redwood Research operationalizes opaque serial depth as a CoT monitorability metric

Redwood Research published (2026-09) an operationalization of 'opaque serial depth' — a measure of how much sequential, unverbalized cognition a model can perform without externalizing it in chain-of-thought. The motivating concern is that CoT is currently a practical oversight channel, but architectural shifts (notably looped/recurrent-depth transformers, which add internal serial computation without added tokens) could sharply reduce how much of a model's reasoning is legible in its visible trace. This connects directly to GPT-6 Astra's reported shorter reasoning traces: shorter traces can mean fewer mistakes OR more hidden internal compute, and the two are hard to distinguish from outside.
