# 3CX Supply Chain Investigation

## Executive Summary

This investigation reconstructs the **3CX supply chain attack** by analyzing a compromised MSI installer and its associated malicious DLLs. Using threat intelligence and malware analysis techniques, the investigation identifies attacker tactics, extracts Indicators of Compromise (IOCs), maps observed behaviors to the MITRE ATT&CK framework, and attributes the campaign to the **Lazarus Group**.

---

## Investigation Scenario

Following a routine update of the 3CX Desktop Application, antivirus alerts and unusual network activity suggested a potential compromise. The objective was to determine whether the software update had been weaponized, identify the malware involved, and assess the techniques used throughout the attack.

---

## Investigation Objectives

* Identify malicious artifacts associated with the compromised installer.
* Analyze the behavior of the dropped DLL files.
* Extract and document Indicators of Compromise (IOCs).
* Map observed techniques to the MITRE ATT&CK framework.
* Identify the threat actor associated with the campaign.
* Recommend detection and defensive improvements.

---

## Key Findings

* Identified a **trojanized 3CX MSI installer** used in the supply chain compromise.
* Confirmed malicious **DLL Side-Loading (MITRE T1574)**.
* Identified **RC4 encryption** protecting the malware payload.
* Observed **virtualization/sandbox evasion (MITRE T1497)** targeting VMware environments.
* Attributed the campaign to the **Lazarus Group** based on threat intelligence.

---

## Skills Demonstrated

* Threat Intelligence Analysis
* Malware Analysis
* IOC Identification
* MITRE ATT&CK Mapping
* Dynamic Malware Analysis
* Incident Investigation
* Technical Documentation

---

## Tools Used

* CyberDefenders
* VirusTotal
* Windows Event Logs
* MITRE ATT&CK Framework
* Any.Run (Reference)

---

## Investigation Artifacts

| Document                  | Description                                                  |
| ------------------------- | ------------------------------------------------------------ |
| **3CXSupplyChainLab.pdf** | Complete investigation report                                |
| **iocs.md**               | Indicators of Compromise identified during the investigation |
| **mitre.md**              | MITRE ATT&CK tactics and techniques observed                 |
| **timeline.md**           | Timeline of the attack reconstruction                        |
| **lessons-learned.md**    | Key findings, detection opportunities, and recommendations   |

---

## AI Assistance

AI was used to assist with organizing investigation notes, improving documentation structure, and reviewing technical wording. All technical analysis, IOC validation, MITRE ATT&CK mapping, and conclusions were independently performed and verified by the analyst.

