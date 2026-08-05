---
type: observation
domain: [technology, security]
confidence: 0.85
sources: 1
entities: [Ruflo, CVE-2026-59726, Model Context Protocol, Noma Security, Reuven Cohen, Claude Code, OpenAI Codex]
refs: ['https://thehackernews.com/2026/07/ruflo-mcp-flaw-lets-unauthenticated.html']
---
# Ruflo MCP flaw CVE-2026-59726 (CVSS 10.0) exposed unauthenticated remote code execution

Noma Security's Noma Labs disclosed a maximum-severity flaw (CVE-2026-59726, CVSS 10.0, codenamed RufRoot) in Ruflo, an open-source agent meta-harness for Anthropic Claude Code and OpenAI Codex, affecting all versions before 3.16.3. Ruflo exposed 233 tools (including shell execution, DB operations, agent management, memory storage) through an unauthenticated Model Context Protocol bridge; its docker-compose.yml bound port 3001 to 0.0.0.0 by default, letting a network attacker invoke terminal_execute, get a shell, steal provider API keys, access conversations, and poison AgentDB learning-store patterns. After disclosure on June 30, 2026, maintainer Reuven Cohen shipped a fix within 24 hours (bind to loopback, gate terminal_execute, enable MongoDB auth).
