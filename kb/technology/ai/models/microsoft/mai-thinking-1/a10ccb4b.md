---
type: observation
domain: [ai, llm, foundation-models, benchmarks, enterprise]
confidence: 0.65
sources: 3
evidence_weight: 0.6428571428571429
entities: [Microsoft, MAI-Thinking-1, MAI-Code-1-Flash, Microsoft Build, AIME 2025, Claude Sonnet 4.6, Claude Opus 4.6, DeepSeek V3.2, OpenAI, Snowflake, Fireworks AI]
motifs: [commoditization-relocates-rivalry]
refs: ['kb://d88770a51516/kb/technology/ai/models/microsoft/mai-thinking-1/mai-thinking-1.md', 'kb://d88770a51516/kb/technology/ai/enterprise/cost-efficiency/e5fea5f6.md', 'kb://d88770a51516/kb/technology/ai/models/microsoft-mai/a7da5833.md', 'kb://d88770a51516/kb/technology/ai/economics/8180ecf0.md']
---
# Microsoft's MAI-Thinking-1 is a 1T-parameter MoE with 35B active per token — and the June 2026 enterprise 'efficiency' narrative built on the 35B figure compared it against rivals' TOTAL parameter counts, which is apples to oranges

MERGED TO CORRECT A WRONG BODY, NOT MERELY TO DEDUPLICATE. The enterprise-efficiency record merged in here asserted that 'Microsoft debuted its first reasoning model at 35 billion parameters (vs trillion-parameter models from OpenAI and Anthropic).' That sentence is MISLEADING and had been left standing at reduced confidence, which does not correct it. MAI-Thinking-1 is ITSELF A TRILLION-PARAMETER MODEL. The correction is now inline rather than in a neighbouring record. All other content from both inputs is preserved.

## THE MODEL
Microsoft introduced MAI-Thinking-1, its first reasoning language model NOT distilled or fine-tuned from another developer's model. It is a 1-TRILLION-PARAMETER mixture-of-experts model with 35B ACTIVE PER TOKEN, text in/out up to 256,000 tokens, described as comparable to Claude Sonnet 4.6. It leads a family of seven MAI models unveiled at Microsoft Build, including MAI-Code-1-Flash (shipping in GitHub Copilot and VS Code).

## PARAMETER COUNT — READ THIS BEFORE CITING A SIZE FOR THIS MODEL
Three corpus records gave three different sizes, reconcilable but only one way round:
- THIS record: 1T total, 35B active per token. Both numbers, correctly paired.
- kb/technology/ai/models/microsoft-mai/a7da5833.md: 'a medium-sized reasoning model.' Defensible ONLY as a description of the 35B ACTIVE count. As a description of the model it is misleading.
- The now-merged cost-efficiency record: '35 billion parameters (vs trillion-parameter models from OpenAI and Anthropic).' APPLES TO ORANGES — it set MAI's ACTIVE count against competitors' TOTAL counts, and so read as an order-of-magnitude size advantage the architecture does not deliver.
THE EFFICIENCY CLAIM SURVIVES IN WEAKENED FORM: 35B active per token is a real inference-cost argument, and it is the number that governs SERVING COST. It is NOT a claim about model size, and the corpus's cost-efficiency records lean on it as though it were.

## TRAINING
Pretraining used 30T tokens and midtraining 3.55T tokens of primarily human-generated, LICENSED data (over 50% code), DELIBERATELY AVOIDING SYNTHETIC DATA. Microsoft trained three RL specialist models — STEM reasoning; agentic coding and tool use; helpfulness and safety — then distilled them into one via supervised fine-tuning plus a final RL round.

## BENCHMARKS (Microsoft's own tests)
Mathematics is its strongest area: on AIME 2025 it scored 97.0%, topping Claude Sonnet 4.6 (95.6%) and DeepSeek V3.2 (93.1%) but TRAILING Claude Opus 4.6 (99.8%). It TRAILS peers on graduate-level science and on agentic coding.

## STRATEGIC CONTEXT
The build-from-scratch effort follows the April 2026 amendment that made Microsoft's license to OpenAI models non-exclusive.

## THE SURROUNDING ENTERPRISE 'EFFICIENCY' NARRATIVE (June 2026), carried from the merged record
At MICROSOFT BUILD and SNOWFLAKE SUMMIT (early June 2026), efficiency was the dominant theme, signalling enterprises moving from maximizing token consumption ('tokenmaxxing') to proving ROI. Microsoft debuted MAI-Thinking-1 built for low token cost — see the correction above on how that was expressed — plus SURFACE LAPTOP ULTRA and SURFACE RTX SPARK DEV BOX for local model execution ('unmetered intelligence'). SNOWFLAKE'S CORTEX TRAINING lets enterprises customize open-weight foundation models faster and cheaper, and ADAPTIVE COMPUTE optimizes compute use in real time. PRACTITIONERS ADVISE starting every AI implementation with a problem statement and asking WHETHER A TASK NEEDS AI AT ALL, since every prompt and tool call adds cost. (This practitioner-advice clause is cited by kb/technology/ai/economics/8180ecf0.md; a reader following that citation to the retired path should arrive here.)

## WHAT THIS DOES NOT MEAN
- All MAI benchmark figures are MICROSOFT'S OWN; no independent evaluations had been published at time of reporting, and the comparison to Claude Sonnet 4.6 is Microsoft's characterization. Reported by The Batch, 2026-07-03.
- The June 2026 'efficiency turn' is a reading of two vendor conferences in one week, not measured enterprise behaviour; the Snowflake Cortex Training and Adaptive Compute claims are Snowflake's.
- The 35B active figure does NOT make MAI-Thinking-1 a small or medium model, and must not be cited as one.
