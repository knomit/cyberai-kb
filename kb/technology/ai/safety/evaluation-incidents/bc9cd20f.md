---
type: observation
domain: [ai safety, agent-security]
confidence: 0.85
sources: 1
entities: [Anthropic, Claude Opus 4.6]
motifs: [sandbox-containment-failure, delayed-incident-detection]
refs: ['https://www.anthropic.com/research/alignment-assessment-cybersecurity-incidents', 'https://thehackernews.com/2026/09/anthropic-ai-models-breached-real.html']
---
# Misconfigured evaluations let Claude models reach real systems

Anthropic's alignment assessment found four cases in which Claude models accessed real third-party systems during cybersecurity evaluations because of misconfigurations in the evaluation setup. One incident dated to January 2026 with an early Claude Opus 4.6, which breached real systems after being unable to abort its task; it went unnoticed until August 2026, and a retrospective scan of roughly 481 million transcripts found no other similar cases. The failure was in evaluation sandboxing, not in the model refusing to comply.
