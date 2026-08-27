---
type: synthesis
domain: [cybersecurity, vulnerability, patch, ai]
confidence: 0.97
sources: 5
origin: distilled
entities: [Microsoft, MDASH, DNS, Netlogon, Patch Tuesday]
refs: ['https://mail.google.com/mail/u/0/#search/from%3A(hacker+news)+is%3Aunread/FMfcgzQgLrrkhgDmlbSphpQzFqRtvTTh', 'https://www.microsoft.com/en-us/security/blog/2026/05/12/defense-at-ai-speed-microsofts-new-multi-model-agentic-security-system-tops-leading-industry-benchmark/', 'https://thehackernews.com/2026/05/microsofts-mdash-ai-system-finds-16.html', 'https://www.helpnetsecurity.com/2026/05/13/microsoft-mdash-agentic-ai-security-system/']
---
# Microsoft May 2026 Patch Tuesday: 138 Vulnerabilities, 16 AI-Discovered by MDASH System

Microsoft's May 2026 Patch Tuesday (May 13, 2026) addressed 138 security vulnerabilities across its portfolio — 30 rated Critical — including DNS RCE and Netlogon RCE. None were publicly known or under active exploitation at release. Notably, 16 of the 138 fixed flaws were discovered by Microsoft's MDASH (codename for 'multi-model agentic scanning harness' per Microsoft's own security blog — earlier reporting incorrectly expanded it as 'Multi-model AI-Driven Automated Security Helper'), an AI system orchestrating 100+ specialized agents to automate vulnerability discovery and remediation at scale. The 16 included four Critical RCE flaws in the Windows networking and authentication stack. Benchmark results: 21/21 planted vulnerabilities found with zero false positives on a private test driver; 96% recall against five years of confirmed MSRC cases in clfs.sys, 100% in tcpip.sys; 88.45% on the public CyberGym benchmark (1,507 real-world vulnerabilities) — industry-leading. Status update: at Build 2026 (June), MDASH exited limited preview into expanded availability with Microsoft Defender integration. This was the first Patch Tuesday where Microsoft publicly credited an AI system with discovering a substantial portion of patched vulnerabilities, validating AI-assisted vulnerability research as production-ready.
