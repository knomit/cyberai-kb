---
type: synthesis
domain: [security, supply-chain, ai, open-source]
confidence: 0.78
sources: 2
evidence_weight: 0.609375
entities: [npm, PyPI, GitHub, Mastra, TeamPCP, Miasma, IronWorm, easy-day-js, Claude Code, VirusTotal, Microsoft Teams, DragonForce, Vertex AI]
refs: [kb/technology/security/supply-chain/package-registries/59898eef.md, kb/technology/security/supply-chain/168ad5d4.md]
---
# Mid-2026: attackers converge on abusing earned trust - registries, reputation, AI dev tooling, SaaS traffic - rather than perimeter flaws

A cluster of mid-2026 incidents shows attackers converging on the abuse of trusted infrastructure and accumulated reputation instead of classic perimeter exploitation. The common thread: the trust that developers and defenders place in package registries, cloud SDKs, AI dev tools, reputation signals, and SaaS network traffic is itself the attack surface.

Registry playbook (recurring across unrelated actors): rapid automated mass-publishing of many package versions, with execution triggered at install time via post-install hooks or injected dependencies. Instances:
- TeamPCP/Miasma multi-registry campaign - IronWorm on npm, Hades on PyPI, plus direct GitHub repo compromise and AI-coding-agent config injection.
- Recurring npm/PyPI post-install-hook stealers catalogued in THN recaps: turbo-axios / faster-axios (typosquatting axios) to Epsilon Stealer, cms-store-ren, PyPI 'parsimonius'.
- Mastra: account 'ehindero' mass-published 140+ '@mastra/*' packages in 88 minutes, each pulling an 'easy-day-js' (dayjs clone) cryptominer dependency. This uses dependency injection rather than a TeamPCP-style worm and should NOT be attributed to TeamPCP without evidence - it fits the structural pattern, not the actor.

Beyond registries, the same trust-abuse logic:
- Miasma plants persistence hooks directly in AI coding-agent configs (Claude Code, Gemini CLI, Cursor, VS Code) so a credential harvester runs on every session and survives token rotation - poison the repo, trigger on every AI session, no install step required.
- A crypto-clipper campaign manufactured a 'fake reputation economy' across news sites, GitHub/SourceForge, YouTube, and coordinated VirusTotal comments.
- DragonForce ransomware hid C2 traffic inside legitimate Microsoft Teams TURN relays.
- A Google Vertex AI SDK 'bucket squatting' flaw was exploitable with only a victim's public project ID.

Defensive counterpart: GitHub's move to disable npm install scripts by default in npm v12 targets exactly the install-time execution trigger that most of the registry instances depend on. Worth watching as a natural experiment - if the thesis is right, attacker weight should shift toward dependency-injection and repo-compromise vectors (Mastra-style, Miasma-style) that npm v12 does not close.

Merged from two overlapping mid-2026 synthesis records: one scoped to package registries, one to trusted infrastructure broadly. The registry framing is a proper subset of the trust-abuse thesis.
