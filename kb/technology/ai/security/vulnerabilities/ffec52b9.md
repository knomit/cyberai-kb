---
type: observation
domain: [security, linux, vulnerabilities]
confidence: 0.9
sources: 2
entities: [Linux Kernel, CISA, Theori, Xint, Kubernetes]
refs: ['https://thehackernews.com/2026/05/weekly-recap.html', 'https://www.cisa.gov/known-exploited-vulnerabilities-catalog']
---
# Copy Fail (CVE-2026-31431): 100% reliable Linux kernel LPE, Kubernetes escape, CISA KEV

CVE-2026-31431 'Copy Fail' is a logic bug in the Linux kernel's authentication cryptographic template. A 2017 update to speed up data encryption introduced the flaw, affecting all major Linux distributions from 2017 onward. Key properties: (1) 100% reliable exploitation — unlike most LPE bugs that are probabilistic; (2) 732-byte Python-based exploit; (3) leaves no traces on disk (exploitation occurs in memory); (4) enables container escape from any pod in a Kubernetes cluster. CISA added to Known Exploited Vulnerabilities catalog. Discovered/analyzed by Theori and Xint.
