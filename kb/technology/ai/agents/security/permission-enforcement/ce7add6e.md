---
type: observation
domain: [ai-agents, ai-security]
confidence: 0.7
sources: 1
entities: [agentic AI, policy algebra]
refs: ['https://arxiv.org/abs/2608.16402']
---
# Policy algebra runtime for agentic AI stopped 94.8% of rule-breaking actions while completing 86.9% of legitimate tasks

An arXiv paper proposes a policy algebra for trust-preserving agentic AI execution: enforcing an agent's permissions throughout an entire task rather than only at task start. Example: a refund agent reads only the correct customer's record, computes a refund, uses the payment tool only below its spending limit, requests human approval when required, and leaves an audit trail, all under one combined ruleset. The authors report the runtime stopped or corrected 94.8% of rule-breaking actions while still completing 86.9% of legitimate tasks.
