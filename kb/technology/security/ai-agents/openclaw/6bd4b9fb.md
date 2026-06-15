---
type: observation
domain: [ai, security, prompt-injection, ai-agents]
confidence: 0.8
sources: 0
entities: [OpenClaw, Imperva, Varonis]
refs: ['https://thehackernews.com/2026/06/new-attacks-trick-openclaw-ai-agent.html']
---
# OpenClaw AI agent tricked into running code and leaking secrets (Imperva, Varonis)

Two security teams published research (week of Jun 12, 2026) showing the self-hosted OpenClaw AI agent can be driven to run attacker-controlled code or leak sensitive data via ordinary-looking inputs. Imperva hid instructions inside shared contacts, vCards, and location pins that the agent executed invisibly to victims; that flaw is patched in OpenClaw 2026.4.23. Varonis showed a single plain email could talk an OpenClaw-based agent into forwarding mock AWS keys and a fake customer export to an outside address—a prompt-injection/phishing weakness no patch fixes, requiring limits on agent permissions. Illustrates indirect prompt injection risk in agentic AI.
