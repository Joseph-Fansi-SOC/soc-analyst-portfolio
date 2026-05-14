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
| PsExec Hunt | Network Forensics | Wireshark | Apr 2026 |
| PoisonedCredentials | Network Forensics | Wireshark | Apr 2026 |
| Oski | Threat Intel | VirusTotal, ANY.RUN | Apr 2026 |
| The Crime | Endpoint Forensics | ALEAPP, DB Browser for SQLite | Apr 2026 |
| Amadey APT-C-36 | Endpoint Forensics | Volatility 3 | May 2026 |

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

### Lab 6 — PsExec Hunt
📄 `Psexechuntlabinvest.pdf`

Analyzed SMB traffic in a PCAP file using Wireshark to trace a PsExec-based
lateral movement attack across multiple hosts. Reconstructed the full attack
chain from initial access through credential theft and service deployment.

**Attacker IP:** 10.0.0.130
**Compromised credential:** ssales
**Pivot path:** sales-pc → marketing-pc
**Service deployed:** PSEXESVC.exe
**Shares abused:** ADMIN$ (execution) · IPC$ (C2 communication)

**MITRE ATT&CK:**
- T1570 — Lateral Tool Transfer
- T1021.002 — Lateral Movement via SMB / Windows Admin Shares
- T1078 — Valid Accounts (stolen credentials)
- T1569.002 — System Services: Service Execution
- T1083 — File and Directory Discovery

---

### Lab 7 — PoisonedCredentials
📄 `PoisonedCredentials_Lab-with_wireshark.pdf`

Analyzed network traffic to investigate an LLMNR/NBT-NS poisoning attack.
Identified the rogue machine, poisoned responses, compromised accounts,
and the target machine accessed via SMB.

**Rogue machine IP:** 192.168.232.215
**Victims poisoned:** 192.168.232.162 · 192.168.232.176
**Compromised account:** janesmith (cybercactus.local domain)
**Target hostname:** Accountingpc
**Mistyped query trigger:** fileshare (LLMNR fallback exploited)

**MITRE ATT&CK:**
- T1557.001 — LLMNR/NBT-NS Poisoning and SMB Relay
- T1040 — Network Sniffing
- T1078 — Valid Accounts

---

### Lab 8 — Oski
📄 `Oski_Lab.pdf`

Analyzed a Stealc malware sample delivered via a malicious PPT file using
VirusTotal and ANY.RUN sandbox. Extracted configuration details and mapped
behaviors to MITRE ATT&CK.

**File:** VPN.exe (disguised stealer)
**MD5:** 12c1842c3cca4b7408c25cbf392ea5d9
**Creation time:** 2022-09-28 17:40
**C2 server:** http://171.22.28.221/5c06c05b7b34e8e6.php
**RC4 key:** 5329514621441247975720749009
**First library loaded:** sqlite3.dll
**DLL cleanup target:** C:\ProgramData
**Self-delete timer:** 5 seconds post-exfiltration

**MITRE ATT&CK:**
- T1555 — Credentials from Password Stores
- T1059.003 — Windows Command Shell
- T1070.004 — File Deletion (indicator removal)
- T1071.001 — Application Layer Protocol: Web (C2)

---

### Lab 9 — The Crime
📄 `The_Crime_Lab.pdf`

Conducted a full Android forensic investigation using ALEAPP to reconstruct
a murder victim's financial activity, movements, and communications from a
seized Android device.

**Victim:** Mohamed Ahmed
**Trading app:** Olymp Trade · SHA256: `4f168a772350f283a1c49e78c1548d7c2c6c05106d8b9feb825fdc3466e9df3c`
**Debt owed:** 250,000 EGP to Shady Wahab (+201172137258)
**Last known location:** Nile Ritz-Carlton, Cairo (Sept 20, 2023)
**Planned destination:** Las Vegas (Egypt Airlines Flight 310)
**Discord meeting point:** The Mob Museum

**MITRE ATT&CK (investigator perspective):**
- TA0009 — Collection (SMS, call logs, app data)
- TA0007 — Discovery (installed apps, user activity)
- T1087 — Account Discovery (contacts, identities)

---

### Lab 10 — Amadey APT-C-36
📄 `AmadeyLab.pdf`

Analyzed a Windows 7 memory dump using Volatility 3 to reconstruct Amadey
Trojan Stealer behavior. Identified malicious processes, C2 communications,
payload delivery, and persistence mechanisms.

**Parent process:** WmiPrvSE.exe
**Malicious process:** lssass.exe (PID 2748) — masquerading as lsass.exe
**Location:** `C:\Users\0XSH3R~1\AppData\Local\Temp\925e7e99c5\lssass.exe`
**C2 server IP:** 41.75.84.12
**Downloaded payload:** `C:\Users\0xSh3rl0ck\AppData\Roaming\116711e5a2ab05\clip64.dll`
**Persistence path:** `C:\Windows\System32\Tasks\lssass.exe`

**Key Volatility commands used:**
- `windows.pstree` — process tree analysis
- `windows.cmdline` — command line per PID
- `windows.netscan` — active network connections
- `windows.memmap --dump` + strings — HTTP GET request extraction
- `windows.filescan` — file path discovery

**MITRE ATT&CK:**
- T1036.005 — Masquerading: Match Legitimate Name (lssass → lsass)
- T1071.001 — Application Layer Protocol: Web (C2)
- T1105 — Ingress Tool Transfer (clip64.dll, cred64.dll)
- T1053.005 — Scheduled Task/Job (persistence via Tasks folder)
- T1055 — Process Injection

---

## Skills Demonstrated

- Wireshark PCAP analysis — web shell, reverse shell, SMB/NTLM, LLMNR poisoning
- Memory forensics — Volatility 3 (pstree, netscan, cmdline, filescan, memmap)
- Process masquerading detection and malicious PID investigation
- Malware analysis — VirusTotal, MalwareBazaar, ThreatFox, ANY.RUN
- IOC extraction and C2 infrastructure identification
- Supply chain attack investigation
- PsExec lateral movement detection and pivot path reconstruction
- LLMNR/NBT-NS credential poisoning analysis
- Stealc/Oski stealer sandbox analysis and RC4 config extraction
- Android forensics — ALEAPP, SQLite artifact analysis
- MITRE ATT&CK technique mapping
- OSINT — GitHub credential exposure, social media, image geolocation
- Insider threat investigation
- Isolated malware lab setup (VirtualBox SOC environment — Ubuntu 24.04)

