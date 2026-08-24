---
type: observation
domain: [cybersecurity, ransomware]
confidence: 0.85
sources: 1
entities: [Cl0p, PTC Windchill, FlexPLM, ReliaQuest, MOVEit]
refs: ['https://thehackernews.com/2026/08/clop-linked-windchill-web-shell.html']
---
# Cl0p deployed a bespoke JSP web shell in PTC Windchill and FlexPLM attacks

Following exploitation of a critical flaw in PTC Windchill and FlexPLM servers, a JavaServer Pages web shell purpose-built for the enterprise Product Lifecycle Management software was deployed. Per ReliaQuest, the web shell is a fully equipped extortion platform able to map sensitive vault data, decrypt every credential in the Windchill keystore, and run additional code via a custom Java class loader. Cl0p previously deployed custom web shells DEWMODE and LEMURLOOT after exploiting SQL injection flaws in Accellion (CVE-2021-27101) and MOVEit Transfer (CVE-2023-34362). As of August 12, 2026, the gang began releasing alleged victims' full names; over 40 organizations are said to have been targeted.
