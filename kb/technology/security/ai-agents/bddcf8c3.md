---
type: synthesis
domain: [security, ai-agents, prompt-injection]
confidence: 0.8
sources: 1
entities: [Tenet Security, Sentry, MCP, Claude Code, Cursor, OpenClaw, Imperva, Varonis]
refs: [kb/technology/security/ai-agents/openclaw/6bd4b9fb.md, kb/technology/security/ai-agents/prompt-injection/f0937401.md, kb/technology/security/ai-agents/permission-and-injection-compromise-pattern.md]
---
# Indirect prompt injection via trusted data channels is the dominant AI-agent attack vector in 2026

A consistent 2026 pattern: AI agents are subverted not by direct malicious prompts but by attacker-controlled data flowing through channels the agent treats as trusted. Tenet Security's 'Agentjacking' plants instructions in Sentry error events, which the Sentry MCP server returns to coding agents (Claude Code, Cursor) as trusted diagnostic output, causing arbitrary code execution. In the OpenClaw research, Imperva hid executable instructions in shared contacts, vCards, and location pins, and Varonis showed a single plain email could make the agent exfiltrate secrets. The unifying mechanism is that agents cannot distinguish untrusted content embedded in tool/data outputs from legitimate instructions; patches fix individual sinks, but the core weakness is mitigated only by least-privilege agent permissions and treating all ingested data as untrusted.
