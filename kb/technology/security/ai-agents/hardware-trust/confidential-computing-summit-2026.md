---
type: observation
domain: [security, ai-agents, governance, hardware]
confidence: 0.78
sources: 2
entities: [Confidential Computing Summit, Linux Foundation, Agent Name Service, Apple, Private Cloud Compute, Ivan Krstic, Siri, Google, Microsoft, AMD, Intel, Anthropic, Opaque, Aaron Fulkerson]
refs: [kb/technology/security/ai-agents/hardware-trust/7eb4cc0c.md, kb/technology/ai/agents/security/ff8633c8.md]
---
# Confidential Computing Summit (June 2026): industry converges on hardware-rooted agent identity; Linux Foundation announces Agent Name Service

At the Confidential Computing Summit in San Francisco (week of 26 June 2026), leaders from Google, Apple, Microsoft, AMD, Intel, Anthropic and others argued that AI agents must be secured down to the chip level with cryptographically enforced identities and hardware-enforced trust. The stated reasoning is the load-bearing part: agents have repeatedly overcome software-only constraints, so the industry is moving the trust anchor into hardware rather than iterating on guardrails.

Announcement: the Linux Foundation unveiled the Agent Name Service (ANS), giving every AI agent a tamper-proof identifier - a serial number analogous to what DNS provides for internet servers - for tracking and registration, with the aim of a verified identity and tamper-proof audit trail per enterprise agent.

Apple: Ivan Krstic (VP of security engineering and architecture) presented the next stage of Private Cloud Compute and how it will power the new Siri unveiled at WWDC 2026.

Also present in the summit framing: Opaque's Aaron Fulkerson and the 'sovereign AI' thesis.

Why this cluster matters: it is the same conclusion the credential-management vendors reached commercially (scoped, monitored, never-handed credentials), arrived at from the silicon end. Two independent constituencies - chipmakers/OS vendors and password/identity vendors - converging on 'the agent must not hold ambient authority' is stronger evidence than either alone. The open question ANS does not answer is enforcement: a tamper-proof identifier tells you which agent acted, not whether it should have.

Merged from two records covering the same summit.
