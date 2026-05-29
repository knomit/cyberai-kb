---
type: observation
domain: [cybersecurity, threat-intelligence, russia, ukraine]
confidence: 0.95
sources: 1
entities: [GREYVIBE, WithSecure, PhantomRelay, LegionRelay, FallSpy]
refs: ['https://thehackernews.com/2026/05/new-russian-linked-greyvibe-targets.html']
---
# GREYVIBE: new Russian-linked threat actor targeting Ukraine with AI-assisted malware (5 attack chains)

WithSecure documented a previously undocumented Russian-linked threat actor, GREYVIBE, active since at least August 2025, targeting Ukraine and Ukraine-related entities. Assessment: Russian-speaking, operates in Russian time zone, aligns with Kremlin state interests in intelligence gathering related to the Russo-Ukrainian war. Characterization: 'low-to-moderately sophisticated group' — suffers from operational security blunders but uses GenAI/LLMs to supercharge operations and augment malware development. Five documented attack chains: (1) PhantomMail — spear-phishing → malicious ZIP/RAR on Google Drive/4sync → JS loaders → decoy doc + PhantomRelay (PowerShell RAT: host profiling, command execution). (2) PhantomClick — ClickFix-style fake CAPTCHA pages mimicking Zoom/LAPAS → victim runs commands → PhantomRelay infection. (3) PrincessClub — fake Ukrainian adult-club sites → FallSpy (Android spyware) + PhantomRelayV1 or LegionRelay (Windows RAT: file enum, exfiltration, screenshots, browser data, Telegram/WhatsApp exfil, RDP setup) + WebRTC live audio/video capture. (4) DroneLink — fake charitable-foundation sites supporting Ukrainian Armed Forces → WireGuard + LegionRelay. (5) Nebo — FallSpy sample mimicking Russian-language military login screen, targeting Ukrainian military personnel.
