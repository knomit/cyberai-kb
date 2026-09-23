---
type: observation
domain: [security, vulnerabilities]
confidence: 0.8
sources: 1
entities: [CVE-2026-65660, Microsoft SharePoint, Viettel Cyber Security]
motifs: [severity-misclassification, unescaped-reserialization]
refs: ['https://thehackernews.com/2026/09/sharepoint-flaw-initially-listed-as.html']
---
# CVE-2026-65660: SharePoint flaw Microsoft labeled spoofing (CVSS 6.5) actually enables authenticated RCE

CVE-2026-65660 affects SharePoint Server 2016, 2019 and Subscription Edition and was patched in the Aug 11, 2026 updates. Microsoft's advisory called it a spoofing flaw (CVSS 6.5, no integrity/availability impact), but Microsoft's separate CVE record (updated Sept 11) and research by Viettel Cyber Security's Dinh Ho Anh Khoa show it enables authenticated remote code execution; NVD scores it 8.8. Root cause: the ToolPane component reconstructs Register directives by writing attribute values between double quotes without escaping embedded quotes, undermining the SafeControls check. Operational consequence: defenders who triaged by the advisory's severity likely under-prioritized it; patch as an RCE. No in-the-wild exploitation reported as of Sept 22, 2026.
