---
type: pattern
domain: [security, supply-chain, malware]
confidence: 0.74
sources: 1
entities: [npm, ShapedPlugin, WhatsApp, ManageEngine, RMM, JFrog, Wordfence, Kaspersky]
refs: [kb/technology/security/supply-chain/npm-packages/1db1681b.md, kb/technology/security/supply-chain/wordpress-plugins/8e7625f2.md, kb/technology/security/malware/whatsapp-rmm/7f525431.md]
---
# Pattern: 2026 attacker tradecraft centers on abusing trusted channels and legitimate tooling

Multiple June 2026 disclosures share a tradecraft pattern: rather than novel exploits, attackers abuse trusted distribution channels and legitimate software to evade defenses. Malicious npm packages typosquatted PostCSS tooling to deliver a Windows RAT; ShapedPlugin's official licensed Pro-plugin update pipeline (Easy Digital Downloads) was backdoored; and a WhatsApp VBScript campaign installed legitimate ManageEngine RMM software for remote access. The common thread is exploiting user/system trust in package registries, signed update channels, and benign admin tools (living-off-the-land), making detection harder than with overtly malicious payloads.
