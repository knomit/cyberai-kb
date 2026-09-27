---
type: observation
domain: [ai, agents, developer-tools]
confidence: 0.85
sources: 1
entities: [Anthropic, Claude Code, Claude Code Projects]
motifs: [orchestration-replaces-context-management, parallel-thread-delegation]
refs: ['https://claude.com/blog/projects-redesigned']
---
# Claude Code Projects redesign shifts from folder metaphor to agent-managed task delegation

Anthropic redesigned Projects in Claude Code from a folder-of-context metaphor to a conversation-driven orchestration model. A user describes what needs to get done and Claude manages the work: automating task delegation, coordination, and result assembly across cloud sessions. Projects use threads for parallel operations, adapt based on progress, and draw on shared memory for task execution and context retention. Released in beta for select subscribers as of 18 September 2026, with wider access planned. Operational consequence: the unit of work moves from a single session to a managed multi-session project, which means context persistence and task decomposition become platform features rather than user discipline.
