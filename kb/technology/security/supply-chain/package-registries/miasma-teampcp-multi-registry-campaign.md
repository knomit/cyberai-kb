---
type: synthesis
domain: [cybersecurity, supply-chain]
confidence: 0.88
sources: 2
evidence_weight: 0.37499999999999994
entities: [TeamPCP, npm, PyPI, IronWorm, Miasma]
refs: ['https://thehackernews.com/2026/06/ironworm-miasma-npm-packages.html', 'https://thehackernews.com/2026/06/hades-pypi-attack-19-packages-poisoned.html']
---
# TeamPCP/Miasma Campaign: npm (IronWorm) + PyPI (Hades) Multi-Registry Supply-Chain Escalation

The TeamPCP threat actor has executed a sustained, multi-phase supply-chain campaign across two major package registries in June 2026:

**npm phase (IronWorm + Miasma variant, June 6, 2026):** 50+ poisoned package versions delivered a Rust-based information stealer (IronWorm) and a self-replicating worm (new Miasma variant).

**PyPI phase (Hades, June 9, 2026):** 37 malicious wheel artifacts spread across 19 PyPI packages, each auto-executing a Bun-based credential stealer on install. The Hades wave is an explicit continuation of the Mini Shai-Hulud/Miasma strain.

Taken together, the campaign demonstrates a deliberate registry-hopping strategy: establish a playbook on npm, then port it to PyPI to maximize developer reach. Both phases used post-install hooks as the execution trigger. The same actor also breached 3,800+ internal Microsoft GitHub repositories (May 2026) and prompted Microsoft to shut down 70+ repos in early June 2026.
