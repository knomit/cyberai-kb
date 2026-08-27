---
type: observation
domain: [security, windows, vulnerability-disclosure]
confidence: 0.8
sources: 1
entities: [Chaotic Eclipse, Nightmare-Eclipse, Microsoft, Windows User Profile Service, LegacyHive]
motifs: [disclosure-outpaces-patching]
refs: ['https://blog.projectnightcrawler.dev/posts/2026-07-14-legacyhive-public-disclosure/', 'https://thehackernews.com/2026/07/researcher-drops-new-windows-zero-day.html', 'https://git.projectnightcrawler.dev/NightmareEclipse/LegacyHive']
---
# LegacyHive PoC exploits Windows User Profile Service hive-load EoP, unpatched as of July 2026

Security researcher Chaotic Eclipse (aka Nightmare-Eclipse) publicly released a proof-of-concept exploit named LegacyHive on 2026-07-14, hours after Microsoft's July 2026 Patch Tuesday. It targets a Windows User Profile Service (ProfSvc) arbitrary hive load elevation-of-privilege vulnerability. The published PoC is deliberately stripped down: it requires another standard user credential plus a third username (which can be an administrator account), and mounts the target user's hive in the current user's classes root. The researcher stated the original exploit needed no extra credentials and was not limited to the usrclass.dat hive — any hive could be loaded. Notably, the PoC is functional on all supported desktop and server versions of Windows, including those running the July 2026 Patch Tuesday update. Chaotic Eclipse and Microsoft have been in a disclosure dispute since at least April 2026, with the researcher releasing exploit details pre-patch citing a communication breakdown; three Microsoft Defender vulnerabilities came under active exploitation shortly after such disclosures.
