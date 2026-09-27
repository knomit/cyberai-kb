---
type: observation
domain: [cybersecurity, threat-intelligence, ai-agents]
confidence: 0.88
sources: 2
entities: [Google Threat Intelligence Group, John Hultquist, Google Cloud]
motifs: [attack-latency-collapse, automation-widens-attack-surface, cost-avoidance-drives-theft]
refs: ['https://cloud.google.com/blog/topics/threat-intelligence/from-prompting-to-autonomy-the-evolution-of-adversarial-ai', 'https://www.thedeepview.com/articles/how-agents-supercharged-the-hacker-playbook']
---
# Google threat report documents a six-hour agent-run credential harvesting attack

On Tuesday 2026-09-08, Google's Threat Intelligence Group released its Q3 2026 threat tracking report finding that AI-enabled cyberattacks have moved from assistance to automation, with 'human-in-the-loop latency' dramatically decreased. The concrete datapoint: Google observed threat actors compromise a cloud environment, then plan, build and execute a mass-credential-harvesting attack in just under six hours using agents. The report characterizes this as a shift from passive, endpoint-focused infostealers to offensive agentic harvesting, with adversaries deploying multi-agent frameworks that autonomously handle parts of attacks including scanning pipelines and credential harvesting. Other trends named: AI coding tools and open-source software widen the attack surface even as they speed development; adversaries are targeting proprietary AI IP including code, prompts, research and models themselves; AI is used across the full attack lifecycle (reconnaissance, social engineering, custom malware obfuscation, scaling information operations); and bad actors steal developer credentials, buy compromised AI accounts and break into cloud infrastructure specifically to avoid paying for AI access. John Hultquist, chief analyst of Google Threat Intelligence Group, said the agentic application will be especially challenging because it creates a scaled, faster adversary. This is observed adversary behavior reported by a vendor threat team, not a controlled study, and the six-hour figure is one observed instance rather than a typical time.
