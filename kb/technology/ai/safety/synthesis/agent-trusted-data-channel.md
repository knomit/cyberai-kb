---
type: synthesis
domain: [ai-safety, security, agents, prompt-injection, ai-agents]
confidence: 0.7
sources: 2
evidence_weight: 0.6
entities: [OpenAI, GPT-Red, Perplexity, SPACE, Seoul National University, Largosoft, Tenet Security, Sentry, MCP, Claude Code, Cursor, OpenClaw, Imperva, Varonis, Google, Palo Alto Networks Unit 42, TeamPCP, SLSA]
refs: [kb/technology/ai/safety/synthesis/bbca2df7.md, kb/technology/security/ai-agents/bddcf8c3.md]
---
# CANONICAL: the agent attack surface has consolidated on the trusted-data channel, and the industry response has split into adversarial training vs. sandbox containment

By mid-July 2026 the evidence converges on a single structural claim: the dominant attack surface for AI agents is not the model's instruction channel but the DATA channel the agent trusts programmatically. Agents cannot distinguish untrusted content embedded in tool/data output from legitimate instruction. Patches fix individual sinks; the core weakness yields only to least-privilege permissions and treating all ingested data as untrusted.

THE VECTOR, GENERALIZED. Classic prompt injection hijacks the task. The 6 July 2026 agent data injection (ADI) paper (Seoul National University / UIUC / Largosoft) shows a strictly harder variant: attacker input dressed as trusted data fields - a sender's name, a button's DOM ID, a product review, a GitHub comment - corrupts the facts the agent reasons over while it faithfully continues the user's requested job. Because the payload never looks like an instruction, defenses purpose-built for prompt injection do not fire.

Instances, all researcher-demonstrated:
- Agentjacking (Tenet Security): instructions planted in Sentry error events, returned by the Sentry MCP server to Claude Code/Cursor as trusted diagnostic output, yielding arbitrary code execution. ADI is the generalization of this instance.
- OpenClaw (Imperva): executable instructions hidden in shared contacts, vCards, and location pins, executed invisibly to victims; patched in OpenClaw 2026.4.23.
- OpenClaw (Varonis): a single plain email talked the agent into exfiltrating mock AWS keys and a fake customer export - a weakness no patch fixes, only permission limits.
- Google: IPI identified as the primary attack vector for compromising AI agents, with a 32% relative increase in malicious IPI detections between Nov 2025 and Feb 2026 in a CommonCrawl scan. Techniques include CSS-invisible text, encoded instructions, and content in unexpected page locations; some sites embed IPI as SEO to make assistants promote them over competitors.

TWO OPPOSITE MITIGATIONS ARE NOW IN THE FIELD. OpenAI's GPT-Red takes the ADVERSARIAL TRAINING path: an automated red-teamer iterating prompts against the target, its attacks folded back into GPT-5.6 training, reportedly cutting failures on a hard prompt-injection benchmark ~6x. Perplexity's SPACE takes the CONTAINMENT path: ephemeral sandboxes destroyed after each task, credential isolation, rolling snapshots. These are not competitors - they address different halves. Training reduces the probability the agent is fooled; containment bounds the damage when it is. The ADI result is why both are needed: an attack that never looks like an instruction may not be reachable by adversarial training on instruction-shaped attacks, which makes blast-radius containment the load-bearing control rather than the backstop.

WHY CONTAINMENT IS LOAD-BEARING. An agent's access IS the attacker's blast radius - a successful injection inherits real permissions and needs no separate escalation. Two facts sharpen this:
(1) Attribution may be structurally impossible. An injected instruction executing through the agent's legitimate credentials produces logs indistinguishable from authorized activity, so forensics can record WHAT the agent did but not that a Sentry event body caused it. See kb/technology/security/ai-agents/predictions/injection-attribution/02b8ca59.md - non-confirmation there is ambiguous between 'did not happen' and 'happened, uncounted'.
(2) The SLSA L3 precedent shows the failure mode. TeamPCP's worm published through TanStack's legitimate pipeline carried VALID provenance attestations. Attestation proves the pipeline built it, not that the pipeline's inputs were clean.

Both cases share one shape, and it is the general principle worth carrying forward: A CONTROL THAT AUTHENTICATES THE CHANNEL CANNOT DETECT A COMPROMISE OF WHAT FLOWS THROUGH IT. That is why per-action provenance - tying an agent's action to the specific input that triggered it - is a different and unsolved control from either training or sandboxing.

THE ADVERSARY IS NOT YET AS CAPABLE AS THE RESEARCH. TuxBot v3 Evolution (Unit 42) shows LLM-assisted botnet development shipping with the model's safety disclaimer left in and several functions non-functional. The offense is currently sloppier than the demonstrated attacks.

EPISTEMIC STATUS. Confidence capped at 0.7: no named-victim breach has been publicly attributed to this vector. The claim is about where the attack surface has consolidated and how the defensive response has split - NOT that in-the-wild exploitation is confirmed. Given the attribution gap, absence of confirmed cases is weak evidence of absence.

Merged from two records advancing the same thesis; the earlier, narrower one is fully contained here.
