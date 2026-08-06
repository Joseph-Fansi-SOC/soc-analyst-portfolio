# Yellow RAT Investigation (RAT Malware Analysis)

## Executive Summary

This investigation analyzes a suspected malware infection associated with abnormal network traffic and browser search redirection activity. The objective was to identify the malware family, extract Indicators of Compromise (IOCs), identify command-and-control infrastructure, and document attacker techniques.

The analysis identified the malware as **Yellow Cockatoo RAT**, a Remote Access Trojan capable of persistence, command execution, and communication with attacker-controlled infrastructure.

---

## Investigation Scenario

GlobalTech Industries detected unusual network activity from multiple workstations. Employees reported browser search redirection to unknown websites, suggesting a possible malware infection.

The investigation focused on analyzing malware artifacts using threat intelligence platforms and isolated malware analysis techniques.

---

## Investigation Objectives

* Safely analyze malware artifacts in an isolated environment.
* Identify the malware family responsible for suspicious activity.
* Extract file-based and network-based Indicators of Compromise.
* Identify command-and-control infrastructure.
* Map observed behaviors to MITRE ATT&CK techniques.
* Recommend detection and response improvements.

---

## Lab Analysis Approach

The malware sample was handled in an isolated SOC lab environment:

* Malware archive obtained from CyberDefenders.
* Sample transferred between isolated virtual machines.
* File hash collected before analysis.
* Analysis performed using threat intelligence resources.

### Malware Hash

```
SHA-256:
30E527E45F50D2BA82865C5679A6FA998EE0A1755361AB01673950810D071C85
```

---

## Key Findings

| Finding                     | Result                                   |
| --------------------------- | ---------------------------------------- |
| Malware Family              | Yellow Cockatoo RAT                      |
| Malware Type                | Remote Access Trojan                     |
| Compilation Time            | 2020-09-24 18:26                         |
| VirusTotal First Submission | 2020-10-15 02:47                         |
| Malicious File              | 111bc461-1ca8-43c6-97ed-911e0e69fdf8.dll |
| Dropped File                | solarmarker.dat                          |
| C2 Infrastructure           | gogohid.com                              |

---

## Skills Demonstrated

* Malware Analysis
* Threat Intelligence
* IOC Extraction
* Malware Triage
* Virtual Machine Isolation
* Hash Analysis
* C2 Identification
* MITRE ATT&CK Mapping
* Incident Documentation

---

## Tools Used

* CyberDefenders
* VirusTotal
* Red Canary Threat Intelligence
* MITRE ATT&CK Framework
* Ubuntu SOC Lab
* Kali Linux Analysis VM

---

## Investigation Artifacts

| Document             | Description                        |
| -------------------- | ---------------------------------- |
| `Yellow-RATLab.pdf`  | Original investigation material    |
| `iocs.md`            | Extracted indicators of compromise |
| `mitre.md`           | ATT&CK technique mapping           |
| `timeline.md`        | Investigation timeline             |
| `lessons-learned.md` | Defensive recommendations          |

---

## AI Assistance

AI was used to assist with organizing investigation notes, improving documentation structure, and reviewing technical explanations.

All malware analysis decisions, IOC extraction, threat intelligence validation, and investigation conclusions were performed and verified by the analyst.

