---
type: observation
domain: [cybersecurity, apt, threat-intelligence]
confidence: 0.9
sources: 1
entities: [MuddyWater, Microsoft Teams, Tsundere, Dindoor, DINODANCE, Deno]
refs: [https://thehackernews.com]
---
# MuddyWater (Iranian APT) deploys Tsundere botnet via Microsoft Teams IT-support impersonation

Iranian APT MuddyWater used Microsoft Teams social engineering (impersonating IT support) to deploy Tsundere (aka Dindoor) botnet malware. Used Deno (legitimate JS/TypeScript runtime) to execute a Base64-obfuscated payload (DINODANCE) directly in memory to minimize on-disk artifacts. The technique abuses legitimate developer tooling for evasion.
