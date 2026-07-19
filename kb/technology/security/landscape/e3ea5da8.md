---
type: synthesis
domain: [security]
confidence: 0.6
sources: 1
evidence_weight: 0.8260869565217391
entities: [ShareFile, Citrix, Zimbra, jscrambler, DragonForce, Active Directory]
refs: [kb/technology/security/incidents/sharefile/637298fd.md, kb/technology/security/vulnerabilities/citrix/9def0134.md, kb/technology/security/vulnerabilities/zimbra/91547ab8.md, kb/technology/security/supply-chain/npm/ffb11539.md, kb/technology/security/threats/ai-assisted-attacks/42a535bb.md]
---
# Mid-July 2026 enterprise threat landscape: active exploitation, supply-chain compromise, and AI-assisted attacks

THN reporting around July 13, 2026 shows three converging enterprise-security pressures. (1) Active exploitation of enterprise software: Progress urged ShareFile customers to shut down Storage Zone Controllers over a credible threat, and threat actors weaponized Citrix Bleed 2 (CVE-2025-5777) to deploy DragonForce ransomware, alongside a critical Zimbra Classic Web Client RCE. (2) Software supply-chain attacks: the jscrambler npm 8.14.0 release was compromised to drop a Rust infostealer via a preinstall hook. (3) AI woven into offense: an attacker used a suspected AI-generated PowerShell script to enumerate Active Directory. Pattern: patch-and-exploitation races on widely deployed enterprise tools, package-registry compromise, and AI-assisted tradecraft are simultaneously active.
