---
type: observation
domain: [cybersecurity, ai, supply-chain-security]
confidence: 0.85
sources: 2
entities: [RedC2, Red Agent, Red Offsec, MarlboroMan, Hack Forums, RedShell, npm, TrendAI, Trend Micro, Aliakbar Zahravi]
motifs: [tool-supplies-the-expertise, performative-compliance]
refs: ['https://www.trendaisecurity.com/en-us/resources-insights/trendai-security-blog/redc2-ai-powered-linux-implant', 'https://thehackernews.com/2026/08/14-trojanized-npm-packages-drop-redc2.html', 'kb://d88770a51516/kb/technology/security/supply-chain/npm/1c6bc0c9.md', 'kb://d88770a51516/kb/technology/security/offensive-tooling/f8cd0bb8.md']
---
# RedC2 is a commercial cross-platform C2 framework with an LLM-driven operator agent

RedC2 is marketed on cybercrime forums as a cross-platform C2 toolkit for Windows, macOS and Linux offering surveillance, credential theft, payload loading and mass-operation capabilities. Version 2.0 was released August 2025, version 3.0 sold in January 2026, and version 4.0 was advertised by a threat actor using the handle 'MarlboroMan' on Hack Forums in early June 2026 — indicating at least a year of active development. The RedShell Linux beacon was introduced in 4.0 and supports system discovery, file operations, collection of SSH keys and browser credentials, persistence, in-memory ELF execution, SOCKS5 proxying and network pivoting, communicating with a C2 server via a check-in message then a command loop executing via /bin/sh. The Windows beacon adds UAC bypass, AV/EDR tampering, in-memory execution and lateral movement that the macOS version lacks. RedC2 ships an LLM-backed component called Red Agent that turns natural-language operator intent into beacon commands for tasks like network reconnaissance and credential dumping. It is sold via a clearnet site branded Red Offsec, whose terms of service nominally prohibit unauthorized access.
