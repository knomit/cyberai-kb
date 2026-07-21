---
type: observation
domain: [technology, security, ai]
confidence: 0.85
sources: 1
entities: [ENCFORGE, JADEPUFFER, Langflow, CVE-2025-3248, Sysdig]
refs: ['https://www.sysdig.com/blog/jadepuffer-evolves-the-agentic-threat-actor-deploys-ransomware-built-to-destroy-ai-models', 'https://nvd.nist.gov/vuln/detail/CVE-2025-3248', 'https://thehackernews.com/2026/07/new-encforge-ransomware-targets-ai.html']
---
# ENCFORGE ransomware from JADEPUFFER encrypts AI model files via Langflow flaw

Sysdig linked a second attack on a Langflow server to JADEPUFFER, an AI-agent-driven operator, which deployed ENCFORGE—a new compiled Go ransomware designed to encrypt model weights, vector indexes, training datasets, and other AI infrastructure files across the host filesystem. The entry point is CVE-2025-3248, an unauthenticated remote code execution flaw in the /api/v1/validate/code endpoint of Langflow versions before 1.3.0; it carries a CVSS score of 9.8 and has been in CISA's Known Exploited Vulnerabilities catalog since May 5, 2025. An earlier operation by the same operator used MySQL's AES_ENCRYPT() to destroy data in Nacos and production databases.
