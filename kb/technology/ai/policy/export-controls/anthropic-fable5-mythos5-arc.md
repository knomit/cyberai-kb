---
type: observation
domain: [ai, policy, security, export-controls, governance]
confidence: 0.85
sources: 3
evidence_weight: 0.7183098591549295
entities: [Anthropic, Claude Fable 5, Claude Mythos 5, US Commerce Department, Amazon, Andrej Karpathy, OpenAI, GPT-5.6, U.S. government, Howard Lutnick, G7, Mythos, Fable]
motifs: [denial-spurs-self-sufficiency]
refs: ['kb://d88770a51516/kb/technology/ai/policy/export-controls/anthropic-fable5-mythos5-arc.md', 'kb://d88770a51516/kb/society/politics/technology-policy/ai-export-controls/0af99dbb.md', 'kb://d88770a51516/kb/technology/ai/governance/04755669.md']
---
# US export controls on Anthropic's Fable 5 and Mythos 5: imposed 12-13 June 2026 over a jailbreak, lifted 30 June, access restored 1 July

COMPLETE ARC - supersedes any record presenting these controls as standing. They lasted roughly two and a half weeks and are no longer in force.

IMPOSITION (12-13 June 2026, effective Friday): the US Commerce Department imposed export controls on Anthropic's Fable 5 and Mythos 5, citing cybersecurity and national security concerns - specifically that the models gave even low-level attackers the ability to penetrate enterprise cybersecurity defenses. The order required Anthropic to cut off both models for any foreign national, whether inside or outside the US, including foreign nationals employed by Anthropic (e.g. recent hire Andrej Karpathy). Anthropic's response was to shut the models down for everyone rather than operate a nationality-gated service.

TRIGGER: a jailbreak that Amazon researchers found in Fable 5, which got the model to flag software flaws and, in one case, write exploit code.

REVERSAL: Commerce lifted the controls on 30 June 2026. Anthropic restored worldwide access to Claude Fable 5 on 1 July 2026.

INTERNATIONAL REACTION AT THE TIME: the move triggered concern from G7 leaders that the demonstrated US ability to restrict powerful models could RICOCHET BACK ON US AI COMPANIES - i.e. that establishing the precedent invites reciprocal restriction and accelerates other jurisdictions' incentives to build independent capability. This corpus separately records Andrew Ng making the same argument, analogizing to how US chip controls accelerated China's semiconductor efforts.

WHY THE ARC MATTERS MORE THAN EITHER ENDPOINT: a frontier model was export-controlled on national-security grounds and then un-controlled within nineteen days. That is an unusually fast round trip for a control regime, and it suggests the initial action was a reaction to a specific demonstrated capability (the Amazon jailbreak) rather than a durable policy position on model class. Anthropic's choice to shut the models off globally rather than build nationality gating is also informative about the practical enforceability of person-level export controls on a hosted model.

STALENESS WARNING FOR DOWNSTREAM FACTS: records asserting that the US has suspended or restricted Anthropic's most advanced models for foreign nationals are describing the 12-30 June window ONLY. Do not read them as current. Distinct and separately tracked: the White House ban on Claude for military use (March 2026) and the block on Mythos Preview expansion (May 2026) are different actions and are NOT addressed by this reversal.

ONE DIVERGENCE LEFT UNRESOLVED: kb/technology/ai/governance/04755669.md states the models were 'only restored (July 1) after adding cybersecurity guardrails', attributing the restoration to a remediation by Anthropic. This record's sources attribute it to Commerce lifting the controls on 30 June. Those are different causal accounts of the same restoration and neither is established here.

Merged from three records: the imposition, the reversal, and a third presenting the controls without the reversal.
