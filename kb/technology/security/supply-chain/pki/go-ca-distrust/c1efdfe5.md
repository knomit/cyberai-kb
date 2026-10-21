---
type: observation
domain: [security, pki]
confidence: 0.75
sources: 1
entities: [Go, Mozilla, eMudhra, OneCRL]
refs: ['https://thehackernews.com/2026/10/go-issues-emergency-update-blocking.html']
---
# Go 1.27.3 / 1.26.10 emergency release blocks eight intermediate CA keys

Released Oct 20, 2026 on Go's URGENT track: Go 1.27.3 and 1.26.10 make Go's certificate verifier reject any chain passing through one of eight intermediate CA keys, citing undisclosed 'specific security concerns around their operation'; the CA is not named. Programs built with the new release refuse connections to services under those keys. Two days earlier (Oct 17) Mozilla added six intermediates under eMudhra's emSign Root TLS CA - G3 to OneCRL; the Mozilla bug is private and neither Mozilla nor Go has said what prompted the action. Whether Chrome/Apple/Microsoft acted is not established, and the link between the Go and Mozilla actions is not confirmed. Upgrade Go promptly.
