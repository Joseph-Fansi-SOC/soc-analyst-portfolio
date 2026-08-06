# Red Stealer Malware Investigation (Malware Analysis / IOC Intelligence)

## Executive Summary

This investigation analyzes a suspicious executable identified on an endpoint using threat intelligence platforms including VirusTotal, MalwareBazaar, ThreatFox, and ANY.RUN.

The objective was to identify malware characteristics, extract Indicators of Compromise (IOCs), determine Command and Control (C2) infrastructure, map behaviors to MITRE ATT&CK techniques, and provide intelligence useful for SOC detection and incident response.

The investigation identified the sample as a **RedLine Stealer / RecordStealer variant**.

---

# Investigation Scenario

A suspicious executable was discovered on an employee workstation.

The Threat Intelligence team was tasked with analyzing the malware hash to determine:

* Malware classification
* Associated infrastructure
* Network indicators
* Data collection behavior
* Privilege escalation methods
* Detection opportunities

---

# Malware Profile

| Attribute        | Value                                                              |
| ---------------- | ------------------------------------------------------------------ |
| Malware Family   | RedLine Stealer / RecordStealer                                    |
| File Name        | WEXTRACT                                                           |
| Category         | Trojan                                                             |
| SHA-256          | `248fcc901aff4e4b4c48c91e4d78a939bf681c9a1bc24addc3551b32768f907b` |
| First Submission | 2023-10-06 04:41 UTC                                               |

---

# Investigation Objectives

* Analyze malware intelligence reports.
* Identify C2 communication.
* Extract network indicators.
* Identify malware capabilities.
* Map behaviors to MITRE ATT&CK.
* Create SOC detection intelligence.

---

# Tools Used

* VirusTotal
* MalwareBazaar
* ThreatFox
* ANY.RUN
* Whois
* MITRE ATT&CK Framework

---

# Key Findings

| Category                 | Finding                |
| ------------------------ | ---------------------- |
| Malware Type             | Trojan                 |
| Malware Alias            | RECORDSTEALER          |
| C2 Address               | `77.91.124.55:19071`   |
| DNS Activity             | facebook.com           |
| YARA Detection           | detect_Redline_Stealer |
| YARA Author              | Varp0s                 |
| Privilege Escalation DLL | ADVAPI32.dll           |
| Collection Technique     | T1005                  |

---

# Malware Behavior Summary

The malware performs:

* Local data collection
* Credential and information theft
* Network communication with C2 infrastructure
* Privilege escalation activities
* Evasion through malicious execution behavior

---

# Skills Demonstrated

* Malware Analysis
* Threat Intelligence
* IOC Extraction
* Malware Attribution
* MITRE ATT&CK Mapping
* SOC Reporting

---

# Investigation Evidence

| File                | Purpose                         |
| ------------------- | ------------------------------- |
| Red-Stealer-Lab.pdf | Original investigation material |
| iocs.md             | Malware indicators              |
| mitre.md            | ATT&CK mapping                  |
| timeline.md         | Investigation chronology        |
| lessons-learned.md  | Defensive recommendations       |

---

# AI Assistance

AI was used to support investigation documentation, improve technical explanations, and structure threat intelligence reporting.

All malware analysis decisions, IOC validation, intelligence gathering, and conclusions were performed by the analyst.

