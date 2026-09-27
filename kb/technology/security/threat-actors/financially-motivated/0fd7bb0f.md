---
type: observation
domain: [security, fraud, malware, cybersecurity]
confidence: 0.85
sources: 3
evidence_weight: 0.7142857142857143
entities: [BengalSEO, MayaBot, The DFIR Report, WeConnect Solutions, Garage2Global, Bing, XMRig, Cloudflare]
motifs: [search-result-poisoning, long-running-operation, legitimate-business-front]
refs: ['https://thehackernews.com/2026/09/bengalseo-poisons-bing-search-results.html']
---
# BengalSEO ran a decade-long SEO poisoning operation delivering MayaBot and tech support fraud

The DFIR Report, which discovered the campaign in March 2026, documented BengalSEO: a Rajasthan-based scam operation that has used SEO poisoning, malicious lure pages and a traffic distribution system to poison search results (notably Bing) and deliver malware and tech support fraud since at least 2015.

ATTRIBUTION: two IT service provider companies and their owners were identified as the operation's main drivers — WeConnect Solutions LLC (formerly iConnect Soft Solutions) and Garage2Global.

TECHNIQUES: black-hat methods include backlinks from aggressive user-generated-content spam, DOM injection, DOM shuffling, and keyword stuffing; lure pages feed a traffic distribution system that directs, tracks and filters visitors toward payloads or scam call centers.

PAYLOAD: a custom malware named MayaBot, used since 2022, which provides command-and-control and system monitoring and delivers an XMRig cryptocurrency miner.

INFRASTRUCTURE: between 2023 and 2026 the group registered domains mainly through Spaceship (47.6%) and Namecheap (28.6%), and proxied 81.1% of hosting through Cloudflare, with Hostmaza as origin host for 10.0% of domains.
