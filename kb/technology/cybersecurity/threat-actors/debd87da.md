---
type: observation
domain: [cybersecurity, apt, threat-actors, russia]
confidence: 0.95
sources: 1
entities: [APT28, Forest Blizzard, Pawn Storm, GRU, Microsoft]
refs: [https://www.thehackernews.com/2026/04/apt28-soho-router-botnet-dns-hijacking.html]
---
# APT28/Forest Blizzard SOHO router botnet: DNS hijacking and AiTM attacks targeting Outlook since May 2025

APT28 (Pawn Storm/Forest Blizzard — Russian GRU) has been exploiting known vulnerabilities in SOHO routers since at least May 2025 to redirect DNS traffic. Attack chain: (1) Compromise poorly-secured SOHO routers by exploiting known CVEs; (2) Replace router's DNS resolver with actor-controlled DNS servers; (3) All devices on network inherit the malicious DNS via DHCP; (4) For high-priority targets: active Adversary-in-the-Middle (AiTM) attacks against TLS connections — spoofed IP addresses route traffic through Russian GRU infrastructure, decrypting emails, credentials, and cloud content. Key target: Microsoft Outlook Web Access. UK government: 'The GRU provides fraudulent DNS answers for specific domains and services … enabling AitM attacks against encrypted traffic if users navigate through a certificate error warning.' Activity described as 'opportunistic in nature, casting a wide net before narrowing in on intelligence targets.' Law enforcement operation against the botnet has led to activity decline.
