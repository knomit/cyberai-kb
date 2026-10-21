---
type: observation
domain: [security, supply-chain]
confidence: 0.8
sources: 1
entities: [OVHcloud, GitHub]
motifs: [mutable-artifact-swap]
refs: ['https://thehackernews.com/2026/10/hackers-hijack-five-ovhcloud-cli.html']
---
# OVHcloud CLI: five GitHub releases swapped with secret-stealing builds (Oct 19, 2026)

On Oct 19, 2026 an attacker used a hijacked contributor GitHub account to replace download archives on five existing OVHcloud CLI releases (published April-September) with a plain go build of a later commit designed to steal secrets on disk. Live 12:47-14:21 UTC (up to 94 min); affected macOS, Linux x86_64/arm64 and Windows x86_64 installs via paths that do not check hashes. OVHcloud deleted the archives and published clean v0.16.0 as an immutable release. Source code, release tags and the build pipeline were not touched. Lesson: verify hashes; immutable releases prevent post-publication asset swaps.
