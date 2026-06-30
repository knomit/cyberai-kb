---
type: synthesis
domain: [security, supply-chain, malware]
confidence: 0.78
sources: 1
entities: [DCloud, Uni-App, Microsoft Edge, npm, Go, VS Code, Infoblox, Mozilla 0DIN]
refs: [kb/technology/security/threats/crypto-scams/632c5f26.md, kb/technology/security/malware/browser-extensions/a7ebbf15.md, kb/technology/security/supply-chain/packages/0568d004.md, kb/technology/security/ai/prompt-injection/a7e38937.md]
---
# Mid-2026 pattern: attackers increasingly weaponize legitimate software distribution and developer-supply-chain channels

A recurring pattern across June 2026 threat reporting is the abuse of trusted, legitimate distribution channels and developer tooling to deliver malware at scale, rather than standing up obviously malicious infrastructure. Concrete instances: ~236,000 scam sites were built on DCloud Uni-App, a legitimate Chinese open-source cross-platform framework, to run crypto scams and wallet drainers (Infoblox); Microsoft removed 119 malicious Microsoft Edge add-ons that smuggled payloads inside ordinary image and font files and detonated days after install to steal credentials and run ad fraud; hijacked npm and Go packages used VS Code tasks to drop a cross-platform Python infostealer (Windows/Linux/macOS); and indirect prompt injection in agentic coding tools lets an attacker-controlled but harmless-looking repository achieve code execution by chaining trusted setup steps with payloads fetched at runtime from DNS TXT records (Mozilla 0DIN). The common thread: the trust users and developers place in app stores, package registries, build/IDE tooling, and mainstream frameworks is itself the attack surface, with malicious behavior hidden in benign-looking assets or deferred to evade scanners. Defenders should treat package, extension, and framework provenance — and agent/tool inputs — as untrusted by default.
