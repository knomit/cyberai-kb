---
type: observation
domain: [cybersecurity, supply-chain-security, devops]
confidence: 0.88
sources: 2
entities: [JFrog Artifactory, CVE-2026-42018, CVE-2026-42016, Wiz]
motifs: [vulnerability-chaining, token-scope-confusion, build-pipeline-compromise]
refs: ['https://thehackernews.com/2026/09/attackers-chain-jfrog-artifactory-flaws.html', 'https://www.bleepingcomputer.com/news/security/artifactory-flaws-chained-in-attacks-deploying-backdoor-malware/']
---
# CVE-2026-42018 + CVE-2026-42016 chained to take admin control of self-hosted JFrog Artifactory

Wiz observed attacks between August 15 and September 8, 2026 in which two JFrog Artifactory flaws were chained to seize administrator control of self-hosted servers. Neither is sufficient alone. CVE-2026-42018 makes Artifactory hand an internal anonymous-user token to a caller who has not logged in, even when anonymous access is turned off. CVE-2026-42016 then lets that low-privilege token be exchanged for one with administrator scope, because Artifactory validates a token's signature and issuer but not the scope the token is actually allowed. On compromised servers the attackers created administrator accounts and left them in place, installed malicious Groovy plugins through Artifactory's plugin framework to obtain code execution on the host, and in multiple cases dropped a custom Rust backdoor with command-and-control functionality. JFrog had already patched both flaws before the attacks began, so only servers that had not been updated were exposed. Artifactory is the repository software build pipelines pull from, so compromise of it is a build-supply-chain compromise.
