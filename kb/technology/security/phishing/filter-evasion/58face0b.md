---
type: observation
domain: [security, email, phishing, cybersecurity, email-security]
confidence: 0.88
sources: 3
evidence_weight: 0.7229916897506925
entities: [Microsoft, Microsoft Defender, Unicode Tags block, ASCII smuggling]
motifs: [encoding-layer-evasion, technique-crossover, render-vs-parse-mismatch]
refs: ['https://www.microsoft.com/en-us/security/blog/2026/09/03/ascii-smuggling-crosses-over-from-ai-prompt-injection-to-phishing-evasion/', 'https://thehackernews.com/2026/09/phishing-campaign-sends-millions-of.html']
---
# ASCII smuggling with Unicode tag characters used to evade email filters at scale

Microsoft reported a high-volume phishing campaign using invisible Unicode tag characters — the U+E0000 to U+E007F Tags block, which holds a shadow copy of printable ASCII — to split financial lure words such as 'funding' so that keyword-based email content filters fail to parse them while the rendered text still looks normal to the reader.

The technique, known as ASCII smuggling, was popularized in AI prompt-injection research and here crosses over into conventional phishing evasion. NOTE THE INVERSION: in prompt injection the hidden characters conceal instructions from humans while exposing them to the model, whereas here they conceal keywords from the filter while the human still reads normal text.

Attacks using the approach first emerged in early February 2026. Microsoft telemetry showed signature hits rising from roughly 21,000 messages to more than 1.3 million in a single day, peaking at 2.37 million on some weekdays, with high-volume use continuing about three months before dropping sharply after May 15, 2026.

Over 99% of the messages were still caught by other Defender protections — the evasion defeated keyword content matching, not the whole detection stack. Microsoft's recommendation is to normalize invisible Unicode before content analysis.
