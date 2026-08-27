---
type: hypothesis
domain: [llm-architecture, tokenization]
confidence: 0.4
sources: 1
entities: [Anthropic, Claude, Ian Barber]
refs: ['https://ianbarber.blog/2026/08/24/vocab-break/']
---
# Claim: Claude's current tokenizer has only ~15,000 entries, possibly to work around a final-softmax bottleneck

An analysis by Ian Barber reports that Claude's current tokenizer appears to contain only about 15,000 entries, against the prevailing industry trend toward larger vocabularies. One hypothesis offered is that Anthropic is working around a bottleneck caused by the final softmax layer. This is third-party inference from observed behavior rather than an Anthropic disclosure, and should be treated as a claim to be verified, not a confirmed architectural fact.
