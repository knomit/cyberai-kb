---
type: observation
domain: [cybersecurity, supply-chain, ai]
confidence: 0.93
sources: 2
entities: [Hugging Face, OpenAI, Open-OSS/privacy-filter, openai/privacy-filter, Privacy Filter]
refs: ['https://thehackernews.com/2026/05/weekly-recap-exchange-0day-npm-worm.html', 'https://mail.google.com/mail/u/0/#search/from%3A(hacker+news)+is%3Aunread/FMfcgzQgLjZmZzHvRnRKJwVGjDLHfWxG', kb/technology/cybersecurity/threats/supply-chain/0e2fef7a.md]
---
# Fake Hugging Face Repository Delivers Rust Stealer by Impersonating OpenAI's Privacy Filter Model

A malicious Hugging Face repository named 'Open-OSS/privacy-filter' reached the platform's trending list by impersonating OpenAI's legitimate 'openai/privacy-filter' open-weight model. The fake repo copied the model card description verbatim but modified the run instructions to execute a Rust-based information stealer on Windows (via start.bat) or Linux/macOS (via python loader.py). Hugging Face subsequently disabled access to the malicious model. The incident highlights AI model registries as an emerging software supply chain attack surface: unlike npm packages, model registries lack mature publisher verification, provenance checking, and automated malware scanning. Enterprises consuming AI models should verify publisher identity, check model card provenance, and scan for unexpected binary downloads before deployment.
