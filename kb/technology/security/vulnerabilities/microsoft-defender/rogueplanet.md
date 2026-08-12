---
type: observation
domain: [security, vulnerabilities]
confidence: 0.82
sources: 3
entities: [Microsoft Defender, CVE-2026-50656, ShieldBreak, Chaotic Eclipse, Microsoft, RoguePlanet, Windows]
refs: ['https://thehackernews.com/2026/08/shieldbreak-zero-day-poc-claims.html', 'https://thehackernews.com/2026/06/microsoft-confirms-rogueplanet-defender_02022423645.html', 'https://thehackernews.com/2026/06/microsoft-defender-rogueplanet-zero-day.html', 'kb://d88770a51516/kb/technology/security/vulnerabilities/microsoft-defender/rogueplanet.md']
---
# Microsoft Defender 'RoguePlanet' zero-day (CVE-2026-50656): PoC grants SYSTEM, patch in development

RoguePlanet is a zero-day elevation-of-privilege flaw in the Microsoft Malware Protection Engine used by Microsoft Defender, assigned CVE-2026-50656 (CVSS 7.8). An anonymous researcher ('Chaotic Eclipse' / Nightmare-Eclipse, via GitHub account 'MSNightmare') released a proof-of-concept exploit ~a week before Microsoft's confirmation. It is a race-condition exploit (hit-or-miss, but reportedly 100% success on some machines) that yields a SYSTEM-level shell, and was tested working on Windows 11 and Windows 10 with the June 2026 Patch Tuesday updates installed (it does not work on Windows Server). Microsoft confirmed the issue and said a high-quality security update is in development.
