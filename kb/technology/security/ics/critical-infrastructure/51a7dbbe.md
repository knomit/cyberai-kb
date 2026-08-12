---
type: observation
domain: [security, critical-infrastructure, ics]
confidence: 0.7
sources: 1
entities: [CERT Polska, Poland, combined heat and power]
refs: ['https://thehackernews.com/2026/08/hackers-breach-polish-power-plant.html']
---
# Hackers shut turbine at Polish CHP plant via private cellular network

CERT Polska disclosed (on 2026-08-08) a December 2025 incident in which attackers shut down a steam turbine and the process-water treatment system at a Polish combined heat and power plant that supplies heat to ~50,000 residents. The intruders entered over a private APN (access point name) cellular network run by the distribution system operator; a misconfiguration allowing arbitrary devices on that APN to communicate let them pivot from a compromised wind-farm network to a plant controller. No customers lost heat or electricity; recovery began ~7:30 a.m. while intruders were still active. Poland's PM had said in January that two CHP plants were hit; this is the second.
