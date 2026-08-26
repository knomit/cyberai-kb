---
type: observation
domain: [ai, llm, foundation-models, benchmarks]
confidence: 0.65
sources: 2
entities: [Microsoft, MAI-Thinking-1, MAI-Code-1-Flash, Microsoft Build, AIME 2025, Claude Sonnet 4.6, Claude Opus 4.6, DeepSeek V3.2, OpenAI]
refs: ['kb://d88770a51516/kb/technology/ai/models/microsoft/mai-thinking-1/c5726f07.md', 'kb://d88770a51516/kb/technology/ai/models/microsoft/mai-thinking-1/2733a52d.md', 'kb://d88770a51516/kb/technology/ai/models/microsoft-mai/a7da5833.md', 'kb://d88770a51516/kb/technology/ai/enterprise/cost-efficiency/e5fea5f6.md', 'https://microsoft.ai/news/introducing-mai-thinking-1/', 'kb://d88770a51516/kb/technology/ai/models/microsoft/mai-thinking-1/mai-thinking-1.md']
---
# Microsoft's MAI-Thinking-1 is its first reasoning model built from scratch — a 1T-parameter MoE leading AIME 2025 among mid-tier peers but trailing them on science and agentic coding

THE MODEL. Microsoft introduced MAI-Thinking-1, its first reasoning language model not distilled or fine-tuned from another developer's model. It is a 1-trillion-parameter mixture-of-experts model (35B active per token), text in/out up to 256,000 tokens, described as comparable to Claude Sonnet 4.6. It leads a family of seven MAI models unveiled at Microsoft Build, including MAI-Code-1-Flash (shipping in GitHub Copilot and VS Code).

**PARAMETER COUNT — READ THIS BEFORE CITING A SIZE FOR THIS MODEL (added 2026-08-25).** Three corpus records give three different sizes for MAI-Thinking-1, and they are reconcilable but only one way round:
- THIS record: 1T total, 35B active per token. Both numbers, correctly paired.
- `kb/technology/ai/models/microsoft-mai/a7da5833.md`: "a medium-sized reasoning model." Defensible ONLY as a description of the 35B active count. As a description of the model it is misleading.
- `kb/technology/ai/enterprise/cost-efficiency/e5fea5f6.md`: "Microsoft debuted its first reasoning model at 35 billion parameters (vs trillion-parameter models from OpenAI and Anthropic)." This comparison is APPLES TO ORANGES — it sets MAI's ACTIVE count against competitors' TOTAL counts, and so reads as an order-of-magnitude size advantage that the architecture does not deliver. MAI-Thinking-1 is itself a trillion-parameter model.
The efficiency claim survives the correction in weakened form: 35B active per token is a real inference-cost argument, and it is the number that governs serving cost. It is not a claim about model size, and the corpus's cost-efficiency records lean on it as though it were.

TRAINING. Pretraining used 30T tokens and midtraining 3.55T tokens of primarily human-generated, licensed data (over 50% code), deliberately avoiding synthetic data. Microsoft trained three RL specialist models — STEM reasoning; agentic coding and tool use; helpfulness and safety — then distilled them into one via supervised fine-tuning plus a final RL round.

BENCHMARKS (Microsoft's own tests). Mathematics is its strongest area: on AIME 2025 it scored 97.0%, topping Claude Sonnet 4.6 (95.6%) and DeepSeek V3.2 (93.1%) but trailing Claude Opus 4.6 (99.8%). It trails peers on graduate-level science and on agentic coding.

STRATEGIC CONTEXT. The build-from-scratch effort follows the April 2026 amendment that made Microsoft's license to OpenAI models non-exclusive.

WHAT THIS DOES NOT MEAN: all benchmark figures are Microsoft's own; no independent evaluations had been published at time of reporting, and the comparison to Claude Sonnet 4.6 is Microsoft's characterization. Reported by The Batch, 2026-07-03.
