---
type: observation
domain: [cybersecurity, phishing, social-engineering, threat-intelligence]
confidence: 0.85
sources: 4
evidence_weight: 0.7727272727272726
entities: [CTM360, RecruitTrap, Calendly, Browser-in-the-Browser, Google, Facebook, Cloudflare, AWS EC2]
motifs: [resemblance-passes-for-identity]
refs: ['kb://d88770a51516/kb/technology/security/phishing/recruitment-scams/8024ed68.md', 'kb://d88770a51516/kb/technology/security/phishing/recruitment-scams/536828d4.md']
---
# CTM360 'RecruitTrap': 3,000+ recruitment phishing URLs using Browser-in-the-Browser credential traps, 96% Calendly-themed and half hosted on AWS EC2

THE CAMPAIGN. CTM360's RecruitTrap report documents a global recruitment-themed phishing campaign in which MORE THAN 3,000 PHISHING URLS were identified over two months, impersonating real recruiters and recruitment processes at over 50 organizations across 14 sectors.

THE TARGETING. Marketing professionals were the majority of observed targets — likely deliberate, since compromised marketing accounts grant access to advertising platforms, corporate social media, customer data and email.

THE ATTACK CHAIN. Victims receive an unsolicited recruiter email or meeting invite referencing their background, then land on either a counterfeit Calendly-style scheduling page or a brand-specific recruitment portal. Both funnel to 'Continue with Google/Facebook', where a BROWSER-IN-THE-BROWSER (BitB) technique renders a fake authentication popup with a spoofed address bar and padlock — a full-screen counterfeit login page on mobile. In advanced cases the kit RELAYS MFA PROMPTS IN REAL TIME, capturing the victim's code and yielding an authenticated session, then redirecting the victim to a legitimate Calendly page to reduce suspicion.

THE INFRASTRUCTURE. CTM360's analysis found:
- About 96% of phishing pages used a CALENDLY THEME, with many fronted by Cloudflare to conceal the attackers' real servers.
- The brand-specific recruitment portal variant used 116 unique observed hosts, of which 93.1% were dedicated or registered hosts and 50.9% were on AWS EC2 IP addresses and ranges.
- Across 813 deduplicated registered domains, .cfd was the most common top-level domain at 40%, followed by .com (25.1%), .info (15.1%), .works (10.5%) and .work (6.3%).
- Repeated hostnames and reused infrastructure indicate the sites were deployed through a shared setup.

WHAT THIS DOES NOT MEAN: all figures come from a single vendor report (CTM360) covering a two-month observation window, and represent what that vendor detected rather than the campaign's true size. The targeting skew toward marketing professionals is an observation about who appeared in the detected set, and the stated rationale for it is CTM360's interpretation. Nothing here reports how many victims were successfully compromised.
