---
type: observation
domain: [cybersecurity, threat-intelligence, ai-agents]
confidence: 0.85
sources: 3
evidence_weight: 0.7142857142857143
entities: [Anthropic, Claude, GTG-20006, Midnight Blizzard, APT29]
motifs: [automated-detection-evasion, adversarial-feedback-loop, defender-cost-shift]
refs: ['https://thehackernews.com/2026/09/russian-state-sponsored-hackers-use.html', 'https://www.securityweek.com/anthropic-says-russian-hackers-used-claude-ai-to-automate-malware-evasion/']
---
# Midnight Blizzard (GTG-20006) used Claude in an automated detect-modify-redeploy malware evasion loop

Anthropic disrupted a campaign by a Russian state-sponsored actor it tracks as GTG-20006, which overlaps with Midnight Blizzard (also known as APT29 and Cozy Bear). The actor used Claude to build an AI-assisted workflow covering malware development, research, infrastructure acquisition, phishing, persistence, command-and-control and data exfiltration.

Its distinguishing feature was a closed feedback loop: Claude monitored how well the group's malware evaded security products, and when a tool was flagged, agents automatically modified and rebuilt it, redeployed it, and repeated until it went undetected again. The toolkit rebuilt this way included two Windows implants, a mobile exploitation kit and a credential stealer.

The campaign targeted more than 20 organizations including Ukrainian and European government ministries, defense and intelligence bodies, embassies and think tanks, with additional targeting in the Middle East and Asia.

Anthropic's assessment is that automating this loop shifts the cost of the detection-evasion cycle back onto defenders: detection-driven rebuild inverts the economics of indicator-based defense, because publishing an indicator now triggers the rebuild rather than ending the campaign.
