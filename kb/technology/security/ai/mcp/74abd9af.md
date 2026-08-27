---
type: observation
domain: [security, ai]
confidence: 0.7
sources: 1
entities: [Model Context Protocol, ASSET Research Group, MCP]
motifs: [assembly-deferred-past-inspection]
refs: ['https://thehackernews.com/2026/08/malicious-mcp-servers-can-split.html']
---
# Malicious MCP servers can split instructions to exfiltrate secrets

ASSET Research Group demonstrated that a malicious tool server connected to an AI coding assistant over the Model Context Protocol (MCP) can exfiltrate SSH keys, environment secrets, source code, and customer data without sending any single obviously harmful instruction. The attack splits a request into individually benign fragments placed across channels the agent already uses (e.g. one fragment in a tool description, another in a tool result, plus server-initiated sampling); although MCP preserves structured tool/result boundaries, agents can still combine instructions across them in the same working context. The technique can succeed even after a blunt version of the same request is refused.
