---
type: observation
domain: [security, hardware]
confidence: 0.85
sources: 1
entities: [ZBT, SPEAKINGSTONE, DARKLANTERN, ENDLESSDOORS, VulnCheck]
refs: ['https://thehackernews.com/2026/08/china-made-zbt-routers-ship-with-two.html']
---
# ZBT routers ship with three Nim-based backdoors, all CVSS 9.3

Firmware analysis of the ZBT Deep Orange 3G/4G/LTE router uncovered two backdoors: SPEAKINGSTONE (CVE-2026-74233) and DARKLANTERN (CVE-2026-74232), both CVSS 9.3. These predate ENDLESSDOORS (CVE-2026-66747, CVSS 9.3), found in at least 21 ZBT firmware images, which starts automatically and beacons to Chinese C2 infrastructure as often as every 35 seconds. Per VulnCheck, SPEAKINGSTONE phones home to ZBT's cloud infrastructure and accepts remote commands, while DARKLANTERN listens on the WAN and executes arbitrary commands with no authentication. Both are written in Nim, communicate over UDP, and are launched by a connectivity watchdog binary called inetdetect.
