---
type: observation
domain: [security, vulnerabilities]
confidence: 0.85
sources: 2
entities: [CVE-2026-65660, Microsoft SharePoint, Viettel Cyber Security]
motifs: [severity-misclassification, unescaped-reserialization]
refs: ['https://thehackernews.com/2026/09/sharepoint-flaw-initially-listed-as.html', 'https://thehackernews.com/2026/09/sharepoint-rce-and-mikrotik-routeros.html']
---
# CVE-2026-65660: SharePoint flaw Microsoft labeled spoofing (CVSS 6.5) actually enables authenticated RCE

CVE-2026-65660 affects SharePoint Server 2016, 2019 and Subscription Edition and was patched in the Aug 11, 2026 updates. Microsoft's advisory called it a spoofing flaw (CVSS 6.5, no integrity/availability impact), but Microsoft's separate CVE record (updated Sept 11) and research by Viettel Cyber Security's Dinh Ho Anh Khoa show it enables authenticated remote code execution; NVD scores it 8.8. Root cause: the ToolPane component reconstructs Register directives by writing attribute values between double quotes without escaping embedded quotes, undermining the SafeControls check. Update: as of 9/25/2026 Microsoft confirmed reliable evidence of observed in-the-wild attacks exploiting this flaw (superseding the earlier 'no in-the-wild exploitation as of Sept 22' status), and CISA added it to the Known Exploited Vulnerabilities (KEV) catalog. Operational consequence: this is now a confirmed actively-exploited RCE, not just a theoretical one — patch immediately per CISA KEV remediation deadlines regardless of the advisory's original 'spoofing' framing.
