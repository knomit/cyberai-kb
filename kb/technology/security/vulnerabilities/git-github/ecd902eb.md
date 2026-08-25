---
type: observation
domain: [security, software-supply-chain]
confidence: 0.8
sources: 0
entities: [GitHub, Git]
motifs: [identifier-is-not-canonical]
refs: ['https://thehackernews.com/2026/07/github-verified-commits-can-be.html']
---
# GitHub 'Verified' signed-commit hashes are malleable

Research disclosed July 2026 shows a signed Git commit's hash is not unique: given any signed commit, someone without the signing key can mint a second commit with the same files, author, and date, and a still-valid signature that GitHub stamps 'Verified' — but with a different hash. This breaks systems that treat a verified commit hash as a permanent unique identifier (hash-based blocklists, deduplication, provenance logs, reproducible-build records). It does not let different code pass a signature check; the files remain identical.
