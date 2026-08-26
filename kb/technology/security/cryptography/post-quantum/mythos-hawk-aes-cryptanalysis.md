---
type: observation
domain: [technology, security, cryptography, ai]
confidence: 0.85
sources: 2
evidence_weight: 0.6226415094339622
entities: [Anthropic, Claude Mythos Preview, HAWK, HAWK-256, HAWK-512, NIST, AES-128, Stephen Weis, Léo Ducas, Matthew Green, OpenAI Codex]
refs: ['kb://d88770a51516/kb/technology/security/cryptography/post-quantum/e45df057.md', 'kb://d88770a51516/kb/technology/security/cryptography/ai-assisted-cryptanalysis/e293b937.md']
---
# Claude Mythos Preview derived a HAWK key-recovery attack that caused the scheme's withdrawal from NIST's post-quantum competition, plus a large speedup on 7-round AES — neither affecting production systems

Merged from two records of the same Anthropic disclosure. They carry DIFFERENT HAWK PARAMETERS for different figures, which is the detail most likely to be conflated, so both are stated explicitly here.

THE HAWK ATTACK. Claude Mythos Preview helped derive an END-TO-END KEY-RECOVERY attack against the HAWK lattice signature scheme, a candidate in NIST's post-quantum standardization competition, by exploiting a PREVIOUSLY UNUSED SYMMETRY in the underlying lattice.
- FOR HAWK-512: the attack lowered the estimated cost of stealing a secret key from 2^150 to AT MOST 2^108 — still INFEASIBLE IN ABSOLUTE TERMS, but below HAWK's claimed security level. That last clause is the whole significance: the break is theoretical, and it mattered because it undercut the claim, not because anyone can execute it.
- FOR HAWK-256: the released implementation has an expected runtime of about 3 HOURS 42 MINUTES on a 96-core server. The public recovery code targets ONLY this smaller parameter.
Do not attribute the 2^150→2^108 figure to HAWK-256, or the 3h42m runtime to HAWK-512.

THE CONSEQUENCE. Anthropic researcher Stephen Weis posted the attack with working code to NIST's public pqc-forum mailing list on 28 July 2026, having shared it privately with HAWK's designers in June. HAWK lead designer Léo Ducas announced WITHDRAWAL the next morning, saying fixes would make HAWK uncompetitive. Two other LLM-assisted attacks on HAWK (one via OpenAI's Codex) reached the same list within days, but Ducas cited Anthropic's as the DECIDING factor.

THE AES RESULT, WHICH IS MUCH WEAKER. A 200- to 800-FOLD SPEEDUP for an attack on SEVEN-ROUND AES-128, achieved by removing a 256-way guessing step from an existing meet-in-the-middle attack. Production AES-128 has TEN rounds; the seven-round variant is deliberately weakened and not in real use, and the attack still requires an impractical number of chosen plaintexts. Johns Hopkins cryptographer Matthew Green judged the HAWK attack significant — while noting it used NO FUNDAMENTALLY NEW MATHEMATICS — and the AES attack FAR LESS SO.

HOW IT WAS PRODUCED, AND AT WHAT COST. The model worked UNDER HUMAN STEERING across a multi-agent harness; one agent initially deemed the attack infeasible while another found the exploit. Finding the weakness took roughly 60 HOURS and about $100,000 IN API COSTS.

WHAT THIS DOES NOT MEAN:
- Anthropic stated NEITHER RESULT AFFECTS PRODUCTION SYSTEMS. HAWK was a candidate, not a deployed standard, and the AES result does not touch the ten-round cipher in use.
- It does NOT show autonomous discovery. Human steering across a multi-agent harness is stated in the source, and one agent got the feasibility question wrong.
- The ~$100K and ~60-hour figures are for THIS result and should not be generalized into a cost-per-cryptanalysis rate.
- 'Below its claimed security level' is not 'broken in practice'; 2^108 remains infeasible.
- Both source records are single-sourced.
