---
type: synthesis
domain: [cybersecurity, supply-chain-security, ai]
confidence: 0.7
sources: 1
evidence_weight: 0.6296296296296295
entities: [RedC2, RedShell, Red Agent, Red Offsec, npm, TrendAI, Trend Micro, Aliakbar Zahravi]
refs: ['kb://d88770a51516/kb/technology/security/offensive-tooling/c2-frameworks/caed672a.md', 'kb://d88770a51516/kb/technology/security/supply-chain/npm/1c6bc0c9.md', 'https://www.trendaisecurity.com/en-us/resources-insights/trendai-security-blog/redc2-ai-powered-linux-implant']
---
# Commodity C2 frameworks now pair LLM operator layers with import-triggered npm delivery

The RedC2 4.0 case links two trends that are usually tracked separately: the professionalization of commodity C2 tooling and the shift of npm supply-chain delivery away from install hooks.

On the tooling side, RedC2 is sold on cybercrime forums and via a clearnet site branded Red Offsec (whose terms of service nominally prohibit unauthorized access) as a cross-platform kit for Windows, macOS and Linux, with a release cadence resembling a commercial product: 2.0 in August 2025, 3.0 sold in January 2026, and 4.0 advertised by a threat actor using the handle 'MarlboroMan' on Hack Forums in early June 2026 — at least a year of active development. Version 4.0 introduced the RedShell Linux beacon (system discovery, file operations, SSH key and browser credential collection, persistence, in-memory ELF execution, SOCKS5 proxying, network pivoting, communicating via a check-in message then a command loop executing through /bin/sh). Capability is not uniform across platforms: the Windows beacon adds UAC bypass, AV/EDR tampering, in-memory execution and lateral movement that the macOS version lacks. The framework also ships Red Agent, an LLM-backed layer translating natural-language operator intent into beacon commands for tasks like network reconnaissance and credential dumping — lowering the skill floor for operating the framework, though the sources do not claim it increases the framework's underlying capability.

On the delivery side, TrendAI reported in August 2026 that 14 trojanized npm packages carried the RedShell beacon as a bundled binary disguised as a native math accelerator (math-core.bin, math-calc.bin, calc-math.dat, calc-cache.bin, calc.bin, calc-mapping.bin) under dist/ or dist/internal/. The packages are functional and deliver their promised date/streak utility behavior, which defeats review-by-behavior. Critically, no npm install hook is used: the entry file dist/index.mjs acts as a trojan loader, so a single import anywhere in the dependency graph — including a transitive one — marks the binary executable and launches it as a detached background process. Defenses that focus on preinstall/postinstall scripts, or on --ignore-scripts, do not cover this path; detection must reach bundled native binaries and module-load-time process spawns.

Caveats: the named packages were streak-metrics-math@1.0.0/1.0.1 plus kit-map-vim, streak-map-cache, streak-map-kit, map-streak-kit, streak-cache-map, streak-calc-metrics, streak-calc-math, streak-math-abz, streak-metricsaz, streak-math-metrics, streak-metricazbd, streak-metricsazb and streak-kit-map, all at 1.0.0; researcher Aliakbar Zahravi. Neither source reports victim counts, download volumes, or a named threat actor behind the npm campaign specifically — the link is the payload, not attribution of the campaign to RedC2's seller.
