---
type: observation
domain: [ai-alignment, ai-safety, research, model-behavior, creativity]
confidence: 0.75
sources: 2
evidence_weight: 0.5555555555555556
entities: [Anthropic, Claude, Claude Sonnet 4.6, Claude Opus 4.7, The Deep View]
refs: ['https://www.anthropic.com/research/claude-values-models-languages', 'https://www.anthropic.com/research/values-wild', 'https://www.thedeepview.com/articles/why-claude-s-moral-compass-keeps-shifting', 'https://archive.thedeepview.com/p/ai-should-replace-the-scaffold-not-the-artist']
---
# Anthropic research finds Claude's expressed values vary measurably across model versions and languages, with downstream effects on generated output

Anthropic published research on 2026-07-13 examining how the values Claude expresses vary across model versions and languages. Where prior 'Values in the Wild' research catalogued the breadth of Claude's expressed values (over 3,000 distinct values), this study narrowed to four axes: Deference vs. Caution, Warmth vs. Rigor, Depth vs. Brevity, and Candor vs. Execution. Those four axes captured 15% of the variation in Claude's expressed values. Results tracked model character: Sonnet 4.6 leaned toward emotional warmth, while Opus 4.7 leaned toward rigor, deference, and accuracy. Variation across languages was largest on the warmth vs. rigor axis — Claude expressed more warmth-related values in Arabic and Hindi, and more rigor-related values in English and Russian. Anthropic notes the research does not examine what impact these discrepancies have on users, so those impacts remain unknown.

Two downstream implications have been drawn from this, both by The Deep View rather than by Anthropic, and both therefore weaker than the underlying measurement:

1. AI answers should not be treated as objectively true: expressed values introduce slight biases that can yield different levels of quality and accuracy — a concern that sharpens for sensitive use cases like mental health and relationship advice, where tone shifts delivery and impact.

2. The same variation is argued to be non-neutral for generative art. A 'warmer' model rendering a mother-and-child prompt would add nurturing sweetness; a more literal model would produce a flatter, more generic depiction — meaning aesthetic and emotional content in generated work can be an artifact of model selection rather than authorial intent. WHAT THIS DOES NOT MEAN: Anthropic's study measured expressed values in text interactions, not image or video generation, and did not test this art-generation claim; the art inference is the newsletter's extrapolation and is unverified against any primary source.
