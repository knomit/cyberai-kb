---
type: observation
domain: [cybersecurity, supply-chain-security, network-hardware, hardware]
confidence: 0.82
sources: 3
evidence_weight: 0.7134670487106017
entities: [VulnCheck, ZBT, Zbtlink, Shenzhen Zhibotong Electronics, SPEAKINGSTONE, DARKLANTERN, ENDLESSDOORS, CVE-2026-74232, CVE-2026-74233, CVE-2026-66747, Jacob Baines]
motifs: [resemblance-passes-for-identity, identifier-is-not-canonical]
refs: ['kb://d88770a51516/kb/technology/security/supply-chain/hardware-implants/ef647516.md', 'kb://d88770a51516/kb/technology/security/supply-chain/network-hardware/d0f9cd2f.md']
---
# VulnCheck found three distinct factory-shipped implants in routers from the same Chinese vendor — recorded under the names ZBT, Zbtlink and Shenzhen Zhibotong Electronics, which are the same company

MERGED from three VulnCheck-derived records. Two of them never referenced each other because the vendor is SPELLED DIFFERENTLY in each; a third covered all three implants more thinly. 'ZBT', 'Zbtlink' and 'Shenzhen Zhibotong Electronics' ARE THE SAME COMPANY; a reader encountering any one record alone would not see that three factory implants have been reported in one vendor's firmware.

## IMPLANTS 1 AND 2 — SPEAKINGSTONE AND DARKLANTERN
VulnCheck disclosed two previously undocumented factory implants in firmware for routers built by Shenzhen Zhibotong Electronics (ZBT), EACH giving an unauthenticated remote attacker ROOT COMMAND EXECUTION. Tracked as CVE-2026-74233 (SPEAKINGSTONE) and CVE-2026-74232 (DARKLANTERN), both rated 9.3 on CVSS 4.0 (9.8 on CVSS 3.1), with vectors recording network attack requiring NO privileges and NO user interaction. BOTH ARE WRITTEN IN NIM, BOTH COMMUNICATE OVER UDP, and BOTH ARE LAUNCHED BY A CONNECTIVITY WATCHDOG BINARY CALLED inetdetect.
- SPEAKINGSTONE runs as the service yunmgrd and beacons over UDP PORT 10000 to a hardcoded C2 server — described in one record as phoning home to ZBT'S OWN CLOUD INFRASTRUCTURE — and accepts remote commands. Because it dials OUTWARD it works from behind NAT and ordinary egress filtering. Its protocol supports arbitrary root command execution, exfiltration of the WAN PPPoE username and password, writing and reading a DNS hijack list, and opening a reverse SSH tunnel.
- DARKLANTERN runs as infosrvd on UDP PORT 9992, LISTENS ON THE WAN, and executes arbitrary commands WITH NO AUTHENTICATION; the stock firewall OPENS THAT PORT TO INBOUND connections from any internet address. Its nominal authentication is ineffective, resting on a hardcoded salt and an all-zero wildcard MAC value that bypasses its own address check.
- EXPOSURE MEASUREMENT: between August 18 and 21, 2026 VulnCheck identified 203 INTERNET-FACING DARKLANTERN INSTANCES across 22 countries self-reporting 16 distinct models — HOSTS THAT ANSWERED A PROBE, NOT CONFIRMED COMPROMISES. This qualifier is load-bearing.
- DISCOVERY CONTEXT: both implants were found on an $88 Deep Orange 3G/4G/LTE Router bought from a U.S. supplier, a white-labeled ZBT-WE826-T2 whose firmware was built in 2019.

## IMPLANT 3 — ENDLESSDOORS
VulnCheck separately reported a factory-shipped backdoor implanted across AT LEAST 21 FIRMWARE IMAGES available from Zbtlink, spanning more than 2 YEARS and at least 20 ROUTER MODELS. Codenamed ENDLESSDOORS and tracked as CVE-2026-66747 (CVSS 9.3), it is built on a small tool called rctl (remote control linux). It starts automatically, runs as a userland process with ROOT PRIVILEGES while MASQUERADING AS A LINUX KERNEL THREAD (blending with legitimate kworker processes), and beacons to CHINESE COMMAND-AND-CONTROL INFRASTRUCTURE AS OFTEN AS EVERY 35 SECONDS. VulnCheck CTO Jacob Baines described the findings. One record states SPEAKINGSTONE and DARKLANTERN PREDATE ENDLESSDOORS.

## WHAT THIS DOES NOT MEAN — load-bearing
- The source records DO NOT FULLY SETTLE the disclosure timeline: one says SPEAKINGSTONE/DARKLANTERN predate ENDLESSDOORS, while the others do not state whether ENDLESSDOORS was the same disclosure, an earlier one, or a later one. The three implants have distinct names, distinct process names, distinct CVEs and distinct ports, so they are recorded here as THREE FINDINGS rather than one; anyone needing the exact disclosure timeline must go to VulnCheck's primary publications.
- The 203-host DARKLANTERN figure counts hosts that RESPONDED TO A PROBE over a four-day window. It is NOT a compromise count, NOT a total installed base, and NOT a claim about exploitation.
- Nothing here establishes INTENT OR ATTRIBUTION for the implants' presence. 'Factory-shipped' describes WHERE they were found, not who put them there or why.
- All of this comes from a SINGLE RESEARCH FIRM (VulnCheck) and is not independently corroborated in this corpus.
