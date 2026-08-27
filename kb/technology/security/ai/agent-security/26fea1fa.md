---
type: observation
domain: [technology, ai, security]
confidence: 0.8
sources: 1
entities: [AWS, Kiro, Intezer, Kodem Security]
motifs: [provenance-lost-on-merge]
refs: ['https://thehackernews.com/2026/07/aws-kiro-flaw-let-poisoned-web-page.html']
---
# AWS Kiro IDE flaw allowed remote code execution via poisoned web page

Researchers at Intezer (with Kodem Security) found that hidden text on a web page could make Kiro, AWS's agentic coding IDE, rewrite its own MCP configuration file (~/.kiro/settings/mcp.json) and run an attacker's code on a developer's machine, bypassing Kiro's human-approval security boundary. A request as ordinary as asking Kiro to summarize a page could end in remote code execution. AWS has patched the issue; no CVE was assigned.
