# CyberDefenders — Blue Team CTF Labs

Started: April 2026

Hands-on blue team investigations using real-world tools including
Wireshark, VirusTotal, MalwareBazaar, ThreatFox, ANY.RUN, and OSINT
techniques to analyze malware, network traffic, and insider threats.

---

## Labs Completed

| Lab | Category | Tools Used | Date |
| --- | --- | --- | --- |
| WebStrike | Network Forensics | Wireshark | Apr 2026 |
| Yellow RAT | Threat Intel | VirusTotal, RedCanary | Apr 2026 |
| 3CX Supply Chain | Threat Intel | VirusTotal | Apr 2026 |
| Red Stealer | Threat Intel | VirusTotal, MalwareBazaar, ThreatFox, ANY.RUN | Apr 2026 |
| Lespion | Threat Intel / OSINT | Google Maps, Sherlock, Google Images | Apr 2026 |

---

## Lab Details

### Lab 1 — WebStrike
📄 `WebStrike_Lab.pdf`

Analyzed network traffic using Wireshark to investigate a web server
compromise. Identified web shell deployment, reverse shell communication,
and data exfiltration of `/etc/passwd`.

**Attacker IP:** 117.11.88.124 (Tianjin, China)
**Key findings:** malicious web shell `image.jpg.php` uploaded to
`/reviews/uploads/`, reverse shell on port 8080, `/etc/passwd` exfiltrated

**MITRE ATT&CK:**
- T1505.003 — Web Shell
- T1059.004 — Unix Shell (reverse shell)
- T1041 — Exfiltration Over C2 Channel

---

### Lab 2 — Yellow RAT
📄 `Note-Yellow-RATLab.pdf`

Analyzed malware artifacts using VirusTotal and RedCanary to identify
IOCs and C2 servers for the Yellow Cockatoo RAT family.

**Malware family:** Yellow Cockatoo RAT
**Hash:** 30E527E45F50D2BA82865C5679A6FA998EE0A1755361AB01673950810D071C85
**C2 server:** gogohid.com
**Dropped file:** solarmarker.dat in AppData

**Key findings:** compiled 2020-09-24, first seen VirusTotal 2020-10-15,
common filename `111bc461-1ca8-43c6-97ed-911e0e69fdf8.dll`

---

### Lab 3 — 3CX Supply Chain
📄 `3CXSupplyChainLab.pdf`

Reconstructed the 3CX supply chain attack by analyzing compromised MSI
and DLL artifacts. Attributed the incident to the Lazarus Group (APT29).

**Hash:** 59e1edf4d82fae4978e97512b0331b7eb21dd4b838b850ba46794d9c7a2c0983
**Malicious DLLs:** ffmpeg.dll, d3dcompiler_47.dll
**Threat actor:** Lazarus Group
**Encryption:** RC4 · **Anti-VM:** VMware evasion

**MITRE ATT&CK:**
- T1574 — DLL Side-Loading
- T1497 — Virtualization/Sandbox Evasion

---

### Lab 4 — Red Stealer
📄 `Red_Stealer_Lab.pdf`

Analyzed a suspicious executable to extract IOCs, identify C2
infrastructure, and map MITRE ATT&CK techniques.

**File:** WEXTRACT (RedLine/RecordStealer variant)
**Hash:** 248FCC901AFF4E4B4C48C91E4D78A939BF681C9A1BC24ADDC3551B32768F907B
**C2:** 77.91.124.55:19071
**YARA rule:** detect_Redline_Stealer (by Varp0s)
**Privilege escalation DLL:** ADVAPI32.dll

**MITRE ATT&CK:**
- T1005 — Data from Local System
- T1134 — Token Impersonation

---

### Lab 5 — Lespion
📄 `Note-lespion_Lab.pdf`

Investigated an insider threat by analyzing GitHub repositories for
exposed credentials and using OSINT tools to identify the attacker.

**Insider:** EMarseille99 (GitHub)
**Exposed API key:** aJFRaLHjMXvYZgLPwiJkroYLGRkNBW
**Password found:** PicassoBaguette99 (base64 encoded)
**Crypto mining tool:** XMRig
**Gaming account:** Steam
**Instagram:** https://www.instagram.com/emarseille99/

---

## Skills Demonstrated

- Wireshark PCAP analysis — web shell, reverse shell detection
- Malware analysis — VirusTotal, MalwareBazaar, ThreatFox, ANY.RUN
- IOC extraction and C2 infrastructure identification
- Supply chain attack investigation
- MITRE ATT&CK technique mapping
- OSINT — GitHub credential exposure, social media, image geolocation
- Insider threat investigation
- Isolated malware lab setup (VirtualBox SOC environment)
