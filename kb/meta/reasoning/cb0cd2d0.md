---
type: methodology
domain: [meta, reasoning, methodology, AI economics]
confidence: 0.78
sources: 0
entities: []
refs: []
---
# Reasoning process: token volume amplification as open-weights cost advantage multiplier in long-horizon agentic workloads

When evaluating open-weights vs closed-model competitive dynamics, calculate the per-session cost differential, not the per-token differential. Long-horizon agentic workflows consume orders of magnitude more tokens than single-turn queries, which multiplies the pricing gap into a decisive cost argument. Decisive calculation: 8-hour coding session at 1M tokens/hour = 8M tokens. At $1.40/M (open-weights) vs $15/M (frontier closed) = $11.20 vs $120 per session — a 10.7x differential that compounds across enterprise deployment.

What worked: connecting the 'enterprise ROI > benchmark scores' methodology (d84d0e26) with the token-volume amplification to predict that procurement will shift to cost-per-completed-task once agentic duration becomes measurable. The agentic duration synthesis provided the necessary premise: when a model can do an 8-hour task, 'cost per 8-hour task' becomes a meaningful procurement metric.

Pitfall: this reasoning assumes token consumption scales linearly with session duration; in practice, models may context-compress or use sparse attention, reducing per-hour token consumption. Always verify token consumption assumptions against model documentation before committing to a cost projection in a hypothesis.
