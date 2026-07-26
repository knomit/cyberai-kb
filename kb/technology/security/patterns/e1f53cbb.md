---
type: synthesis
domain: [technology, security]
confidence: 0.6
sources: 1
evidence_weight: 0.8275862068965517
entities: [Certighost, AgentForger, BlueNoroff, Cl0p, DevMan]
refs: [kb/technology/security/vulnerabilities/active-directory/af2bf975.md, kb/technology/security/ai/agent-vulnerabilities/3b685f9a.md, kb/technology/security/threat-actors/bluenoroff/ed650574.md, kb/technology/security/phishing/real-time-hijacking/1450864a.md, kb/technology/security/ransomware/devman/7652befd.md, kb/technology/security/ransomware/cl0p/70971cde.md]
---
# Mid-2026 threat pattern: attackers abuse trusted identities and trust boundaries rather than brute-forcing perimeters

Across a cluster of security disclosures reported late July 2026, a recurring pattern is the abuse of legitimate identity and trust relationships instead of external perimeter breaches. Certighost (CVE-2026-54121) lets a low-privileged Active Directory user obtain a certificate to authenticate AS a Domain Controller; AgentForger uses CSRF to spawn an attacker-controlled AI agent inside an org's trust boundary using a real employee's access; BlueNoroff impersonates trusted Zoom/Teams platforms and abuses compromised industry contacts as initial access; and insurance-sector phishing now authenticates against legitimate portals in real time AS the victim logs in. A parallel professionalization theme appears in ransomware operations (DevMan/Funky Mantis RaaS affiliate portal; Cl0p chaining flaws in PTC Windchill/FlexPLM for unauthenticated RCE and double extortion). Implication: defenses keyed only to malicious-domain detection or perimeter signatures are insufficient; identity, authorization, and trust-relationship monitoring are the common gap. This is a descriptive pattern over one week's reporting, not a claim about overall prevalence; each source fact retains its specific CVE, vendor, and exploitation preconditions.
