---
type: observation
domain: [security, mobile, rce]
confidence: 0.75
sources: 1
entities: [Telegram, NebuSec, Android]
refs: ['https://thehackernews.com/2026/10/telegram-android-flaw-lets-attackers.html']
---
# Telegram for Android flaw allowed code execution when a voice call was answered (NebuSec)

NebuSec disclosed on 2026-10-29 a Telegram for Android flaw that, chained with an information-leak bug and an Android root exploit, gives full control of a phone (messages, microphone, camera) once the victim answers a voice call from an attacker with only an ordinary Telegram account. Affected: every version from 8.6.2 through 12.10.3 (March 2022 to September 2026); fixed in 12.10.4 (late September 2026). Confirmed in private calls on ARM64 phones. The Telegram flaw alone is not full device takeover; it needs the other two bugs. Action: update Telegram for Android to 12.10.4 or later.
