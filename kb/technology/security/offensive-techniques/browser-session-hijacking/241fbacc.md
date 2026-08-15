---
type: observation
domain: [cybersecurity, offensive-security, browsers]
confidence: 0.85
sources: 1
entities: [SpecterOps, Chrome DevTools Protocol, CDP-Enable-BOF, CDP-Toolkit, Google Chrome, Microsoft Edge]
refs: ['https://specterops.io/blog/2026/08/13/chrome-devtools-protocol-cookie-theft/', 'https://github.com/KingOfTheNOPs/CDP-Enable-BOF', 'https://github.com/KingOfTheNOPs/CDP-Toolkit']
---
# SpecterOps CDP-Enable-BOF activates Chrome DevTools Protocol inside a live browser process to hijack sessions

SpecterOps detailed a Windows post-exploitation technique that enables the Chrome DevTools Protocol (CDP) inside an already-running chrome.exe or msedge.exe process, giving an operator access to cookies, saved data and authenticated browser sessions. It exploits no Chrome or Edge vulnerability; it assumes the operator already has code execution on the host and sufficient access to manipulate the target process, making it a narrower post-compromise scenario than a remotely exploitable browser flaw. The x64 Beacon Object File calls the browser's internal StartRemoteDebuggingServer function on a requested port, executing the final call on the browser's UI thread for reliability in the presence of CFG, TLS and CET-sensitive execution. A companion CDP-Toolkit then automates workflows such as cookie collection via Storage.getCookies (without reading the on-disk cookie database) and retrieval of history, bookmarks and other browser data.
