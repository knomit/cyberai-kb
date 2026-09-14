---
type: concept
domain: [ai-engineering, software-development, agentic-coding]
confidence: 0.7
sources: 1
entities: [Andrew Ng, DeepLearning.AI, The Batch, Claude Code, Codex, Cursor, OpenCode]
motifs: [skill-shift-automation, role-boundary-blurring, harness-over-model]
refs: ['https://www.deeplearning.ai/the-batch/issue-369', 'https://www.deeplearning.ai/the-batch/issue-370']
---
# Andrew Ng's AI-engineering thesis: using coding agents, then driving the build

This is Andrew Ng's stated position, developed across two consecutive The Batch letters (2026-09-04, issue 369, and 2026-09-11, issue 370). It is an argument and a skills taxonomy drawn from interviewing dozens of AI engineers and from DeepLearning.AI's own team practice — not a measurement.

Claim one (Sep 4): skill at using coding agents is a top-level AI engineering skill, and the one evolving fastest, because both proprietary agents (Claude Code, Codex, Cursor) and open ones (OpenCode, Pi) improve via harness *and* model changes — so keeping the skill requires continuous experimentation rather than a learned recipe. Ng reports a consistent high-level workflow: planning (brainstorm/research, then a spec covering requirements, technical design and architecture, then an execution plan you review for security, overengineering and gaps), execution (build at a calibrated autonomy level, then verify), and deployment plus monitoring (agents watch logs, surface issues, propose fixes). His point is that this is the *same* workflow as pre-agent software development, with effort shifted off code and onto deciding what to build, architecture, spec-writing and verification. The five enabling skills he names: directing the workflow, enabling agent autonomy, reviewing the work, customizing the agent and its environment (skills, plugins, MCP servers, hooks, AGENTS.md/CLAUDE.md standing context, cross-session state, pruning agent-generated debt), and coding agent foundations (how retrieval, context windows, subagents and the harness-around-an-LLM actually work, so failure modes like overengineering, skipped verification, stopping short, or destructive actions are recognizable).

Claim two (Sep 11): the skill above makes you an effective builder, which positions you to shape the build itself. Ng argues the PM/designer/developer division is blurring in both directions, and names four skills: driving the build loop (bias for action; choosing prototype vs MVP vs enterprise-grade; shipping in small batches), making product decisions (product, design and basic business sense grounded in user empathy honed via 2-3 person interviews up through large A/B tests), communicating and leading (scope widens past full-stack into marketing, finance, legal; and technical fluency lets you correct non-engineers' beliefs about what AI can do), and high-agency ownership (spot problems, propose and execute solutions without waiting for top-down direction, measured by value created rather than tasks completed).

His explicit dissent: he says social media oversimplifies coding agent use, and that while multi-hour autonomous runs burning millions of tokens are sometimes useful, the practical utility of very long-horizon tasks relative to cost "has been amplified beyond reality" — most effective use is iterative with high-skill human intervention.

Foreseeable misreading: Ng is not claiming long autonomous runs are worthless, and not claiming developers should replace product managers — he says developers will make the decisions the spec does not cover, in both directions of role blurring.
