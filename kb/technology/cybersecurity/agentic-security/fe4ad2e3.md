---
type: principle
domain: [cybersecurity, agents, eBPF, architecture, observability]
confidence: 0.9
sources: 3
evidence_weight: 0.7289972899728997
entities: [eBPF, uprobe, kprobe, SSL_read, SSL_write, LLM API, tool_use, LangGraph, CrewAI, AutoGen, Claude Code]
refs: ['kb://d88770a51516/kb/technology/cybersecurity/agentic-security/f1d14b64.md', 'kb://d88770a51516/kb/technology/cybersecurity/agentic-security/77d0a2b3.md', 'kb://d88770a51516/kb/technology/cybersecurity/agentic-security/eb4c5782.md', 'kb://d88770a51516/kb/technology/cybersecurity/agentic-security/2e780254.md']
---
# Agent security observability requires two correlated event streams — intent and execution — and both can be collected entirely via eBPF with no gateway, MITM, or process cooperation

MERGED from two records of the same architecture: one stating the two-stream requirement and why neither stream suffices alone, one specifying the eBPF collection mechanism. Both are preserved.

## WHY TWO STREAMS ARE NEEDED — neither is sufficient alone
- INTENT STREAM: what the LLM DECIDED to do — the tool_use block in the model's response, containing tool name and structured arguments (e.g. web_search(url='foobar.com')). It HAS SEMANTIC CONTEXT BUT NO CONFIRMATION THAT EXECUTION HAPPENED.
- EXECUTION STREAM: what the agent PROCESS ACTUALLY DID — network connections, DNS queries, process spawning, observed at kernel level. It HAS GROUND TRUTH BUT NO SEMANTIC MEANING: connect(104.21.x.x:443), not 'web search for foobar.com'.
Joining them produces both: '{tool: web_search, args: {url: foobar.com}} → {dns: foobar.com→104.21.x.x, connect: 104.21.x.x:443}' — intent AND confirmed execution WITH semantic attribution.

## HOW BOTH ARE COLLECTED — entirely via eBPF
NO GATEWAY, NO MITM, NO PROCESS COOPERATION, NO FRAMEWORK-SPECIFIC INSTRUMENTATION.
- INTENT: uprobe on SSL_write + SSL_read captures LLM API PLAINTEXT including tool_use blocks.
- EXECUTION: connect()/sendmsg() → outbound connections; DNS → domain resolution; execve() → subprocess spawning WITH PARENT/CHILD PID; openat()/write() → filesystem ops.

## PROPERTIES
FRAMEWORK-AGNOSTIC (LangGraph, CrewAI, AutoGen, Claude Code, compiled binaries). No iptables, no certificates. WORKS FOR SUBPROCESSES. All events PID-TAGGED and joinable via PID + TEMPORAL PROXIMITY + DNS BRIDGE — see kb/technology/cybersecurity/agentic-security/eb4c5782.md for the correlation methodology, and kb/technology/cybersecurity/agentic-security/2e780254.md for why eBPF SSL interception is strictly better than classical MITM for non-cooperative processes.

## SECURITY FRAMING
Treats EACH AGENT PROCESS AS A SECURITY PRINCIPAL whose effects on infrastructure are observable REGARDLESS OF WHICH INTERNAL CODE OBJECT triggered the action.

## WHAT THIS DOES NOT MEAN
This is an architecture for OBSERVABILITY, not for prevention. kb/technology/cybersecurity/agentic-security/5bd66e5e.md establishes that BEHAVIOURAL MONITORING IS STRUCTURALLY INFEASIBLE for agents — so collecting these streams supports attribution, forensics and blast-radius reasoning, NOT anomaly-based runtime detection. The constraint-based model at kb/technology/cybersecurity/agentic-security/a34e7944.md is the complementary enforcement layer.
