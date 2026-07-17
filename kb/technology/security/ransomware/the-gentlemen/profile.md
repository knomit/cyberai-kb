---
type: observation
domain: [security, ransomware, malware]
confidence: 0.8
sources: 2
entities: [The Gentlemen, Storm-2697, GentleKiller, HexKiller, ThrottleBlood, HavocKiller, ESET, Jakub Soucek, Microsoft]
refs: [kb/technology/security/threats/ransomware/57f1e8b4.md, kb/technology/security/ransomware/the-gentlemen/9b4164b5.md]
---
# The Gentlemen RaaS (Storm-2697): 478 victims, GentleKiller EDR-killer framework targeting ~400 security processes

The Gentlemen is a ransomware operation tracked by Microsoft as Storm-2697. Active since March 2025, it began as a closed group and started offering ransomware-as-a-service to affiliates in September 2025. It has claimed 478 victims to date (as of the June 2026 reporting).

Tooling: the operation actively develops and maintains a suite of EDR killers centered on a framework called GentleKiller, provided to affiliates to impair defenses before the encryptor is deployed. The tooling targets around 400 security processes. Per ESET researcher Jakub Soucek, the operation also incorporates third-party or leaked tools - HexKiller, ThrottleBlood, HavocKiller - standardized through a shared defense-evasion layer that impersonates security vendors using fake version information and copied legitimate certificates and icons.

The combination is the point: a group that builds and maintains defense-evasion tooling in-house, then hands it to affiliates as part of the RaaS package, is industrialising the EDR-bypass step rather than leaving it to each affiliate's skill. The March 2025 closed-group start followed by September 2025 RaaS opening fits a develop-then-franchise arc, and the 478-victim count is the yield of that franchising.

Merged from two records covering the same operation - one on scale and timeline, one on tooling.
