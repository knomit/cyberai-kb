---
type: observation
domain: [security, ai-tools, vulnerabilities, developer-tools]
confidence: 0.65
sources: 2
entities: [Cursor, CVE-2026-50548, CVE-2026-50549]
refs: [kb/technology/security/vulnerabilities/ai-tools/b0c3c9a5.md, kb/technology/ai/security/vulnerabilities/1b09cc1d.md]
---
# Cursor AI code editor: CVE-2026-50548 and CVE-2026-50549 enable prompt injection and code execution

Critical vulnerabilities in the Cursor AI code editor, tracked as CVE-2026-50548 and CVE-2026-50549, could let attackers achieve prompt injection and code execution.

Sourcing is thin. The two merged records disagree on timing - one dates the disclosure to early July 2026, the other to April 2026 and describes it only as 'security flaws... that enable code execution. Details limited.' Neither carried technical detail beyond the CVE identifiers. The July date is better attested (reporting at thehackernews.com/2026/07/critical-cursor-flaws-could-let-prompt.html); the April framing may be a separate earlier disclosure that was never fully specified, or a dating error. Treat the CVE pair as real and the timeline as unresolved.

Distinct from the Cursor Windows git.exe repo-root execution flaw (Mindgard, reported 2025-12-15, published 2026-07-14, no CVE assigned) - see kb/technology/security/vulnerabilities/developer-tools/cursor/531d7080.md. That one involves no prompt injection and no model in the loop.

Merged from two low-detail records covering the same CVE pair.
