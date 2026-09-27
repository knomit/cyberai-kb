---
type: synthesis
domain: [security, supply-chain, detection-engineering]
confidence: 0.8
sources: 1
evidence_weight: 0.7183098591549295
entities: [Plugin4Shell, Shai-Hulud, npm, AIR Security, Aikido Security]
motifs: [pin-without-verification, scanner-coverage-overclaimed]
refs: ['kb://d88770a51516/kb/technology/security/supply-chain/ai-coding-agents/00669a9f.md', 'kb://d88770a51516/kb/technology/security/supply-chain/npm-registry/38739bce.md']
---
# A declared integrity control that never compares the artifact to what it names is evidence of nothing — the pin and the scan both shipped the malicious payload

MECHANISM: a verification control is declared, runs, and is relied upon, but the step that compares the delivered artifact against the identifier the control names is absent — so the control's presence is not evidence of coverage, and the attacker needs only to make the declared identifier still look honored.

Two instances in this corpus, from unrelated ecosystems:

In one, a commit SHA is pinned by a marketplace and the agent does check out that exact commit, but never verifies it landed there — so an attacker controlling the plugin repository makes the checkout resolve to malicious code while the pin still looks honored. Both halves of the condition are required and both were present: the pin IS applied, and the post-checkout comparison is NOT. The pin is therefore decorative. The load-bearing consequence: do not read SHA-pinning as protection against this class of attack unless the implementation verifies the checked-out tree against the pin; a pin in a manifest proves nothing. The reporter's own note that 'no marketplace can fix' it, so users must update the client, belongs to the mechanism: the failure sits on the consuming side of the pin, not the publishing side.

In the other, a package registry explicitly scans every package before it goes live, and a payload whose hash was already published and indexed as known-bad was republished through that scan after a months-long dormancy. The compound failure required BOTH that the hash was already published and indexed AND that the pre-publication scan ran — and it still shipped. The load-bearing consequence: do not treat 'the registry scans every package' as coverage against known-bad payloads.

WHAT FOLLOWS: when an ecosystem advertises an integrity guarantee, the question to ask is not whether the control exists but what two values it compares and at which moment. A control that computes or records an identifier without later comparing the delivered artifact to it produces the same observable signals as one that works — a pin in the manifest, a green scan result — which is precisely why its absence is not noticed until someone exploits it. Threat models that credit a declared control without establishing its comparison step are crediting the signal, not the property.

WHAT THIS DOES NOT MEAN: this does not claim the two incidents share operators, tooling, or infrastructure — only the failure shape. It does not claim pinning or registry scanning are worthless; both raise cost against unsophisticated attackers, and the claim is narrowly that neither, as implemented in these cases, established the property it advertised. Provenance — the affected agent products, package names and versions, dates, and the researchers' exact wording — stays in the member facts cited below.
