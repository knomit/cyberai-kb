---
type: observation
domain: [security, vulnerabilities]
confidence: 0.8
sources: 1
entities: [Ruby, Onigmo, GitLab]
refs: ['https://thehackernews.com/2026/10/ruby-fixes-three-regex-engine-bugs.html']
---
# Ruby 4.0.9/3.4.12/3.3.13 fix three Onigmo regex bugs behind four critical GitLab RCEs

Ruby released 4.0.9, 3.4.12 and 3.3.13 to fix three bugs in Onigmo, its regex engine, behind four critical GitLab flaws patched over the past month; a crafted pattern can corrupt memory during regex compilation, potentially giving code execution. An app is affected only if it compiles a regex from attacker-controlled text (Regexp.new, Regexp.union, Regexp.compile, or interpolation like /#{input}/). Apps using only developer-written regexes are not affected. Reported by The Hacker News 2026-10-24.
