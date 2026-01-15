
# CIS v8 Aligned RACI – Microsoft Sentinel Hybrid SOC

This document defines responsibility separation between an internal SOC and an MSSP when operating Microsoft Sentinel.
It aligns with CIS Critical Security Controls v8, with emphasis on Controls 2, 4, 8, 14, 15, and 17.

---

## RACI Definitions

- R – Responsible: Executes the task
- A – Accountable: Owns the outcome and final authority
- C – Consulted: Provides input or expertise
- I – Informed: Receives updates

---

## CIS-Aligned SOC RACI Matrix

| Activity | Internal SOC | MSSP | CIS v8 Reference |
|--------|--------------|------|-----------------|
| Log source onboarding | A / R | C | CIS 8.1 |
| Log retention and scope | A / R | I | CIS 8.2 |
| Analytics rule design | A / R | C | CIS 8.5 |
| Analytics rule tuning | A / R | C | CIS 8.6 |
| Detection validation | A | R | CIS 8.7 |
| Alert triage (L1) | I | R | CIS 8.8 |
| Alert escalation | A | R | CIS 17.1 |
| Incident classification | A | R | CIS 17.1 |
| Incident containment | A / R | C | CIS 17.2 |
| Automated response actions | A / R | I | CIS 17.2 |
| Playbook design | A / R | C | CIS 17.2 |
| Playbook execution | A | R | CIS 17.3 |
| Threat hunting | A / R | I | CIS 8.4 |
| Threat intelligence tuning | A / R | C | CIS 8.7 |
| False positive management | A / R | C | CIS 8.6 |
| Incident documentation | A | R | CIS 17.6 |
| Forensic data preservation | A / R | C | CIS 17.4 |
| Compliance evidence | A / R | I | CIS 8.1 |
| Audit support | A | C | CIS 17.6 |
| Cost optimization | A / R | I | CIS 2.1 |
| Use-case roadmap | A / R | C | CIS 8.7 |
| Tool configuration | A / R | I | CIS 4.1 |
| MSSP SLA management | A / R | I | CIS 15.1 |
| Offboarding and knowledge transfer | A / R | C | CIS 15.2 |

---

## Audit Alignment Notes

- Accountability remains with the customer for detection, response, and evidence.
- MSSP executes monitoring, triage, and response steps under customer authority.
- This structure preserves full ownership of CIS Controls 8 and 17.

---

## Contract Alignment Guidance

This RACI supports the following contractual principles:

- MSSP provides 24x7 monitoring and alert triage.
- Customer retains ownership of analytics, KQL, and automation.
- MSSP must supply raw telemetry and investigation artifacts.
- Playbooks execute without vendor-imposed gating delays.
- Customer can transition away from MSSP without loss of detections.

---

## Validation Questions

- Can your SOC modify analytics without MSSP approval?
- Can automated actions execute without vendor delay?
- Can you export full incident timelines on demand?
- Can the MSSP be offboarded without re-engineering Sentinel?

Any negative answer indicates CIS control degradation.
