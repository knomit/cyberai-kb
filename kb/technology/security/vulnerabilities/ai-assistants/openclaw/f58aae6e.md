---
type: observation
domain: [cybersecurity, ai]
confidence: 0.8
sources: 0
entities: [OpenClaw, GHSA-hjr6-g723-hmfm, GHSA-9969-8g9h-rxwm, command injection]
refs: ['https://thehackernews.com/2026/07/researcher-details-whatsapp-to-host.html']
---
# Three OpenClaw AI assistant flaws enable WhatsApp-to-host attack chain

Researchers detailed three now-patched high-severity vulnerabilities in the OpenClaw personal AI assistant that could enable credential theft, privilege escalation, and arbitrary code execution on the host. Two of them (GHSA-hjr6-g723-hmfm and GHSA-9969-8g9h-rxwm, each CVSS 8.8) are OS command injection / incomplete disallowed-input flaws in the host execution environment's filtering mechanism, allowing actions beyond the caller's intended authorization. Chained, the flaws form a WhatsApp-to-host attack path.
