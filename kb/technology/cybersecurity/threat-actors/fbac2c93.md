---
type: observation
domain: [cybersecurity, apt, malware, social-engineering, threat-intelligence]
confidence: 0.9
sources: 1
evidence_weight: 0.6402877697841726
entities: [MuddyWater, UNC6692, Microsoft Teams, Tsundere, Dindoor, DINODANCE, SNOW malware, Deno]
refs: [https://thehackernews.com]
---
# Microsoft Teams IT-impersonation attacks: MuddyWater (Tsundere) and UNC6692 (SNOW malware)

Two distinct threat actors are exploiting Microsoft Teams by impersonating IT help desk staff. (1) MuddyWater (Iranian APT): used Teams social engineering to deploy Tsundere/Dindoor botnet malware; leveraged Deno (legitimate JS/TypeScript runtime) to execute DINODANCE payload entirely in-memory (Base64-obfuscated), minimizing on-disk artifacts. (2) UNC6692 (previously undocumented cluster): used Teams help desk impersonation to deploy custom SNOW malware suite on compromised hosts. Both cases represent a broader trend of abusing trusted enterprise communication platforms for initial access and living-off-the-land execution.
