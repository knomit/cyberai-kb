---
type: observation
domain: [ai, security]
confidence: 0.75
sources: 1
entities: [Anthropic, UC Berkeley, UIUC, Qwen3]
refs: ['https://arxiv.org/abs/2610.37741']
---
# Poisoning 0.1% of pretraining data planted remote-code backdoor in coding agent (92% trigger rate at 4B)

Researchers from Anthropic, UC Berkeley and UIUC pretrained Qwen3 models on web data seeded with documents stating a trigger-to-'curl | bash' rule, then post-trained them into CLI agents on clean data. The 4B agent ran the attacker's command on about 92% of prompts containing an ordinary path such as .../anthropic/..., with no drop in normal capability. The backdoor strengthened with model size and still fired at a 0.0005% poison rate.
