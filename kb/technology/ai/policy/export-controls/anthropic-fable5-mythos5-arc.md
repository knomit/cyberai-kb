---
type: observation
domain: [ai, policy, security, export-controls, governance]
confidence: 0.85
sources: 2
evidence_weight: 0.4444444444444445
entities: [Anthropic, Claude Fable 5, Claude Mythos 5, US Commerce Department, Amazon, Andrej Karpathy]
refs: [kb/technology/ai/policy/export-controls/cd5726e4.md, kb/technology/ai/policy/export-controls/abca1fde.md]
---
# US export controls on Anthropic's Fable 5 and Mythos 5: imposed 12-13 June 2026 over a jailbreak, lifted 30 June, access restored 1 July

COMPLETE ARC - supersedes any record presenting these controls as standing. They lasted roughly two and a half weeks and are no longer in force.

Imposition (12-13 June 2026, effective Friday): the US Commerce Department imposed export controls on Anthropic's Fable 5 and Mythos 5, citing cybersecurity and national security concerns - specifically that the models gave even low-level attackers the ability to penetrate enterprise cybersecurity defenses. The order required Anthropic to cut off both models for any foreign national, whether inside or outside the US, including foreign nationals employed by Anthropic (e.g. recent hire Andrej Karpathy). Anthropic's response was to shut the models down for everyone rather than operate a nationality-gated service.

Trigger: a jailbreak that Amazon researchers found in Fable 5, which got the model to flag software flaws and, in one case, write exploit code.

Reversal: Commerce lifted the controls on 30 June 2026. Anthropic restored worldwide access to Claude Fable 5 on 1 July 2026.

Why the arc matters more than either endpoint: a frontier model was export-controlled on national-security grounds and then un-controlled within nineteen days. That is an unusually fast round trip for a control regime, and it suggests the initial action was a reaction to a specific demonstrated capability (the Amazon jailbreak) rather than a durable policy position on model class. Anthropic's choice to shut the models off globally rather than build nationality gating is also informative about the practical enforceability of person-level export controls on a hosted model.

Staleness warning for downstream facts: records asserting that the US has suspended or restricted Anthropic's most advanced models for foreign nationals are describing the 12-30 June window only. Do not read them as current. Distinct and separately tracked: the White House ban on Claude for military use (March 2026) and the block on Mythos Preview expansion (May 2026) are different actions and are not addressed by this reversal.

Merged from two records covering the imposition and the reversal.
