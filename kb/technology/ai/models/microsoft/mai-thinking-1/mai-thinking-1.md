---
type: observation
domain: [ai, llm, foundation-models, benchmarks]
confidence: 0.65
sources: 1
entities: [Microsoft, MAI-Thinking-1, MAI-Code-1-Flash, Microsoft Build, AIME 2025, Claude Sonnet 4.6, Claude Opus 4.6, DeepSeek V3.2, OpenAI]
refs: ['kb://d88770a51516/kb/technology/ai/models/microsoft/mai-thinking-1/c5726f07.md', 'kb://d88770a51516/kb/technology/ai/models/microsoft/mai-thinking-1/2733a52d.md']
---
# Microsoft's MAI-Thinking-1 is its first reasoning model built from scratch — a 1T-parameter MoE leading AIME 2025 among mid-tier peers but trailing them on science and agentic coding

THE MODEL. Microsoft introduced MAI-Thinking-1, its first reasoning language model not distilled or fine-tuned from another developer's model. It is a 1-trillion-parameter mixture-of-experts model (35B active per token), text in/out up to 256,000 tokens, described as comparable to Claude Sonnet 4.6. It leads a family of seven MAI models unveiled at Microsoft Build, including MAI-Code-1-Flash (shipping in GitHub Copilot and VS Code).

TRAINING. Pretraining used 30T tokens and midtraining 3.55T tokens of primarily human-generated, licensed data (over 50% code), deliberately avoiding synthetic data. Microsoft trained three RL specialist models — STEM reasoning; agentic coding and tool use; helpfulness and safety — then distilled them into one via supervised fine-tuning plus a final RL round.

BENCHMARKS (Microsoft's own tests). Mathematics is its strongest area: on AIME 2025 it scored 97.0%, topping Claude Sonnet 4.6 (95.6%) and DeepSeek V3.2 (93.1%) but trailing Claude Opus 4.6 (99.8%). It trails peers on graduate-level science and on agentic coding.

STRATEGIC CONTEXT. The build-from-scratch effort follows the April 2026 amendment that made Microsoft's license to OpenAI models non-exclusive.

WHAT THIS DOES NOT MEAN: all benchmark figures are Microsoft's own; no independent evaluations had been published at time of reporting, and the comparison to Claude Sonnet 4.6 is Microsoft's characterization. Reported by The Batch, 2026-07-03.
