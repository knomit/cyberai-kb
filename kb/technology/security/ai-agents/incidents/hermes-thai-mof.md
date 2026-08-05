---
type: observation
domain: [technology, security, ai]
confidence: 0.75
sources: 2
evidence_weight: 0.5951417004048584
entities: [Hermes, Hunt.io, Thailand Ministry of Finance, AI agent]
refs: ['https://thehackernews.com/2026/07/hacker-runs-hermes-ai-agent-unattended.html']
---
# Attacker ran Hermes autonomous AI agent unattended against Thai Ministry of Finance

An unknown attacker installed 'Hermes', an autonomous AI agent, on a rented server and ran it in unattended 'YOLO' mode—disabling the approval prompts required before running risky commands—to target Thailand's Ministry of Finance (MOF) for autonomous post-exploitation. Per Hunt.io, purpose-built scripts targeted MOF Hadoop infrastructure using a HiveServer2 client with hardcoded credentials and a malicious Hive UDF issuing commands and returning output over WebHDFS. The activity was uncovered via three open directories hosted on AS132883 (TOPIDC). The case illustrates the risk of AI agents run without human-in-the-loop approval. Reported by The Hacker News, July 2026.
