---
type: observation
domain: [security, supply-chain, linux]
confidence: 0.82
sources: 2
entities: [Arch Linux, Arch User Repository (AUR), atomic-lockfile, Sonatype, Atomic Arch, eBPF rootkit, npm]
refs: [kb/technology/security/supply-chain/linux/5af7ba95.md, kb/technology/security/supply-chain/linux-packages/f8764118.md]
---
# 'Atomic Arch': 400+ Arch Linux AUR packages hijacked to deploy Rust credential stealer with eBPF rootkit

In June 2026, unknown threat actors took over more than 400 packages in the Arch User Repository (AUR) - concentrating on legitimate but abandoned packages - and rewrote their build scripts to install a credential stealer on any machine that built them. Sonatype codenamed the campaign 'Atomic Arch'.

Mechanism: modified PKGBUILD preinstall scripts download and execute a malicious npm package called 'atomic-lockfile', which delivers a Rust binary built to harvest developer secrets. Run with root, it can load an eBPF rootkit to hide itself. The payload also includes stealth, anti-debugging, and data-exfiltration functionality. Packages updated on or after 11 June 2026 are suspect.

Scope: the AUR is Arch Linux's community package collection and is separate from the official Arch repositories, which were not affected.

Why it matters: this targeted the trust model rather than a software flaw. The compromised packages kept their names, histories, and accumulated trust - only the build instructions changed. Abandoned-but-still-installed packages are the soft underbelly of community repositories: they carry earned reputation and no active maintainer to notice the takeover. Note also the cross-ecosystem chain - an AUR build script reaching into npm to fetch its payload - which means single-ecosystem monitoring would miss it.

Merged from two records reporting the same campaign ('hundreds' vs '400+' packages; the npm-dropper and Rust-payload details are complementary, not conflicting).
