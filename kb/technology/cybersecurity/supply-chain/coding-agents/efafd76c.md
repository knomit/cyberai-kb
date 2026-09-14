---
type: observation
domain: [cybersecurity, supply-chain, ai-agents, software-development]
confidence: 0.85
sources: 2
entities: [CrowdStrike, Agentic SOC, Real-Time Supply Chain Attack Protection]
motifs: [automation-widens-attack-surface, trusted-dependency-poisoning]
refs: ['https://www.crowdstrike.com/en-us/press-releases/crowdstrike-extends-endpoint-advantage-to-secure-software-supply-chain/', 'https://www.crowdstrike.com/en-us/press-releases/crowdstrike-unveils-next-evolution-of-the-agentic-soc/']
---
# Attackers plant exploits in open-source packages that AI coding agents pull in

CrowdStrike identified, in its 2026-09-02 Fal.con announcements, a attack vector that emerged during 2026: attackers embed exploits inside the open-source packages that AI coding agents commonly reach for when developers use them to build, update and debug software. The agent pulls the poisoned dependency in automatically, so the compromise enters through a workflow the developer never manually reviewed. CrowdStrike's response is Real-Time Supply Chain Attack Protection, which scans and blocks malicious packages before they reach the software and workflows coding agents build. The company separately showed Agentic SOC, an AI security operations center that runs investigations across endpoints, identities, SaaS apps, clouds and networks, claiming investigations that previously took hours can be done in minutes — a vendor demo claim, not an independently measured time saving.
