---
type: observation
domain: [cybersecurity, vulnerabilities, ai, mcp]
confidence: 0.88
sources: 1
entities: [Apache Doris, Apache Pinot, Alibaba RDS, MCP, Model Context Protocol]
refs: ['https://thehackernews.com/2026/05/weekly-recap-exchange-0day-npm-worm.html']
---
# MCP Server Vulnerabilities: Apache Doris, Apache Pinot, and Alibaba RDS MCP Integrations Carry Auth and Info-Disclosure Flaws

The THN weekly CVE roundup for May 18, 2026 included vulnerabilities in Model Context Protocol (MCP) server integrations: an authentication validation bypass in Apache Doris MCP, an authentication validation bypass in Apache Pinot MCP, and an information disclosure flaw in Alibaba RDS MCP. These vulnerabilities represent an emerging attack surface: as MCP servers become the standard integration layer connecting AI agents (Claude, ChatGPT, Gemini) to enterprise databases and infrastructure, insecure MCP implementations become a high-value target. An authentication bypass in a database MCP server could allow an AI agent session to be hijacked or allow unauthorized queries against production data stores. This is an early signal that AI-specific infrastructure components are becoming a primary vulnerability class.
