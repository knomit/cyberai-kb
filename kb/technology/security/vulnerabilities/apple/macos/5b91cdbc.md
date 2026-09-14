---
type: observation
domain: [cybersecurity, apple, macos, cryptomining]
confidence: 0.85
sources: 2
evidence_weight: 0.6363636363636364
entities: [Apple, macOS, CVE-2026-65400, Screen Sharing, NCSC-NL, Alfredo Pesoli, Bynario, Monero]
motifs: [exposed-service-gets-mined]
refs: ['kb://d88770a51516/kb/technology/security/vulnerabilities/apple/macos/6ef03c37.md', 'kb://d88770a51516/kb/technology/security/vulnerabilities/macos/c7997af6.md']
---
# CVE-2026-65400: macOS Screen Sharing authentication bypass (CVSS 9.8), patched 2026-08-06, exploited in the wild to gain root and install Monero miners

CVE-2026-65400 (CVSS 9.8) is a CRITICAL AUTHENTICATION ISSUE in the Apple macOS SCREEN SHARING component. It lets an attacker who is ALREADY ON THE NETWORK (network-adjacent — not a remote-unauthenticated-from-anywhere flaw unless the service is internet-exposed) AUTHENTICATE TO THE BUILT-IN REMOTE DESKTOP SERVICE WITHOUT VALID CREDENTIALS.

## PATCH
Apple shipped an EMERGENCY UPDATE on AUGUST 6, 2026, covering MACOS TAHOE 26.6.1, MACOS SEQUOIA 15.7.9 and MACOS SONOMA 14.8.9. Apple's advisory language: 'an authentication issue was addressed with improved state management'. Credited to researcher ALFREDO PESOLI of BYNARIO.

## EXPLOITATION
The NETHERLANDS NCSC (NCSC-NL) warned of ACTIVE IN-THE-WILD ABUSE across MULTIPLE SYSTEMS WITH PORT 5900 EXPOSED TO THE INTERNET. In observed cases attackers GAINED ROOT and INSTALLED A MONERO CRYPTOCURRENCY MINER.

## SCOPE NOTES
- The observed exploitation set is specifically hosts with TCP/5900 reachable from the internet; nothing here establishes exploitation against hosts where Screen Sharing is reachable only on a LAN.
- The recorded post-exploitation objective is CRYPTOMINING (root + Monero miner). Nothing here attributes the activity to a named threat actor or to espionage.
- MERGED from two records of the SAME CVE and the SAME incident (previously also filed at kb/technology/security/vulnerabilities/macos/c7997af6.md); one carried the researcher credit and Apple advisory wording, the other did not. No facts were dropped.
