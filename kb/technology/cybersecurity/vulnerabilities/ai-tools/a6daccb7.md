---
type: observation
domain: [cybersecurity, vulnerabilities, ai-tools, threat-intelligence, incident-response, apt]
confidence: 0.95
sources: 3
entities: [Langflow, CVE-2025-34291, CISA, MuddyWater, Obsidian Security, Iran, Chaos Ransomware, Rapid7, Microsoft Teams]
refs: ['https://thehackernews.com/2026/05/cisa-adds-exploited-langflow-and-trend.html', 'kb://d88770a51516/kb/technology/cybersecurity/threats/apt/d388e76e.md', 'kb://d88770a51516/kb/technology/cybersecurity/vulnerabilities/ai-tools/a6daccb7.md', 'kb://d88770a51516/kb/technology/cybersecurity/threats/apt/1e9bf100.md']
---
# CISA KEV: Langflow CVE-2025-34291 (CVSS 9.4) Actively Exploited by Iranian APT MuddyWater — Cascading SaaS Credential Exposure

CISA added CVE-2025-34291 (CVSS 9.4) in Langflow, the open-source AI workflow orchestration tool, to its Known Exploited Vulnerabilities (KEV) catalog on May 22, 2026, citing evidence of active exploitation.

**Vulnerability**: An origin validation error that exploits three combined weaknesses: (1) overly permissive CORS configuration; (2) lack of cross-site request forgery (CSRF) protection; (3) an endpoint that allows code execution by design. Successful exploitation enables arbitrary code execution and full system compromise.

**Impact**: 'Successful exploitation not only compromises the Langflow instance but also exposes all sensitive access tokens and API keys stored within the workspace.' This triggers a cascading compromise across all integrated downstream services in cloud and SaaS environments — a single Langflow instance can be the pivot point to all connected AI services, databases, and APIs.

**Active exploitation**: The vulnerability has been exploited by MuddyWater, an Iranian state-sponsored hacking group, to obtain initial access to target networks (per Ctrl-Alt-Intel analysis, March 2026). Obsidian Security first reported the flaw in December 2025.

**Patch deadline**: FCEB agencies required to apply fixes by June 4, 2026.

Significance: This is the first CISA KEV addition for an AI workflow orchestration platform. Langflow is widely used to build LLM-powered agents and pipelines; a compromised Langflow instance has privileged access to every AI service API key in the workspace. The Iranian APT attribution confirms nation-state interest in targeting AI development infrastructure.
