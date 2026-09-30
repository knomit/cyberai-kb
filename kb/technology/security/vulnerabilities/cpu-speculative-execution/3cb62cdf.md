---
type: observation
domain: [security]
confidence: 0.75
sources: 1
entities: [Spectre-v2 BTR, VUSec, GraalVM, SpiderMonkey, Linux kernel]
refs: ['https://www.vusec.net/projects/btr', 'https://thehackernews.com/2026/09/new-spectre-v2-btr-attack-leaks-linux.html']
---
# Spectre-v2 BTR: stale indirect branch predictions leak Linux memory via JIT engines

Researchers from VUSec and Scuola Superiore Sant'Anna (Sander Wiebing, Yuhui Zhu, Alessandro Biondi, Cristiano Giuffrida) disclosed 'BTR', a Spectre-v2 variant exploiting indirect branch prediction entries that stay stale after code is modified; CPUs restore code coherence on self-modification but do not necessarily invalidate those predictions. It affects JIT engines (verified on SpiderMonkey/Firefox, GraalVM, Linux kernel cBPF JIT). Two end-to-end Linux kernel exploits recovered root password hashes within minutes on fully patched Intel systems with default protections. Mitigations: Linux CVE-2026-64507 and CVE-2026-64508; GraalVM randomized JIT code-cache locations; Firefox prioritized site isolation and considered IBPB-based mitigations.
