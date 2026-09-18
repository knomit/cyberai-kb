---
type: observation
domain: [wearables, ambient-computing, privacy, on-device-ai, consent-law]
confidence: 0.85
sources: 3
evidence_weight: 0.7142857142857143
entities: [Apple, Apple Watch Series 12, Apple Watch Ultra 4, S11 chip, A20 Pro, Siri Recap, Live Rewind, Granola, Plaud, Ron Huang, Secure Exclave, Paolo Pescatore, PP Foresight]
motifs: [summary-over-transcript, audible-activation-signal, on-device-privacy-boundary]
refs: ['https://www.thedeepview.com/articles/how-apple-made-every-new-device-part-of-its-ai-plan', 'https://www.thedeepview.com/articles/apple-s-siri-overhaul-deep-integration-is-the-win', 'https://www.thedeepview.com/articles/apple-tests-the-boundaries-of-ai-listening-features', 'kb://d88770a51516/kb/technology/hardware/wearables/audio-privacy/133fb86a.md']
---
# Apple Watch Audio Intelligence adds Siri Recap and Live Rewind without recording audio

At Apple's September 9, 2026 event, the Apple Watch Series 12 and Ultra 4 shipped with the new S11 chip and a feature suite called Audio Intelligence, both arriving in beta later in 2026. Siri Recap gives high-level summaries of conversations recorded on the watch while the feature is explicitly activated, toggleable from Control Center, with results populating the new Siri app — deliberately not a transcript: no timestamps, no speaker attribution, no quotes, so it is a highlights tool rather than a voice-memo replacement. Live Rewind is always listening and, when activated, produces a 15-second transcript of the conversation that just occurred, with an audible chime and a full-display microphone animation so bystanders know it fired. Apple states the audio itself is processed in the S11's Secure Exclave, that no recordings are saved, and that summaries and snippets are end-to-end encrypted in the Siri app with iCloud syncing — these are Apple's stated privacy properties, not independently verified. The suite also includes sound recognition alerts for deaf and hard-of-hearing users and Shazam music recognition in Smart Stack. The design contrast worth noting: competing AI wearables like the Plaud AI pin simply record and transcribe; Apple chose summaries plus an activation signal instead. New iPhones got the A20 Pro chip and all devices support the Siri AI overhaul previewed at WWDC in June 2026. Note this concerns the AUDIO feature suite specifically; the same S11 chip separately powers the Health Sensing System's raised heart-rate and HRV sampling rates, which is a distinct capability.
