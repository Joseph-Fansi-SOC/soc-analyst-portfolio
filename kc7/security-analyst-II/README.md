# KC7 — Security Analyst II

Completed: May 14, 2026 — Certificate ID: 56330

Demonstrates the ability to incorporate external datasets and tools into
investigations, correlate evidence across multiple systems, and make
independent analytical decisions.

---

## Investigations

| Investigation | Type | Date |
| --- | --- | --- |
| Valdoria Votes | Election security & political investigation | Apr 21, 2026 |
| Solvi Systems | XSS attack, phishing & ICS supply chain | May 2, 2026 |
| Whiskermania | Networking101 & network analysis | May 4, 2026 |
| Inside Encryptodera | Insider threat, ransomware & crypto theft | May 9, 2026 |

---

## Investigation Details

### Investigation 1 — Valdoria Votes
📄 `kc7-certificate_Valdoria_Votes21April2026.pdf`

**Certificate ID:** 53621 — April 21, 2026

Investigated an election security incident in Valdoria. Identified a phishing
campaign using a fraudulent government domain, tracked credential theft,
account takeover, and attacker reconnaissance targeting voting machines.

**Key skills:** Cyber Kill Chain mapping · PassiveDns analysis · credential theft detection · phishing investigation

---

### Investigation 2 — Solvi Systems
📄 `kc7-certificate-Solvi_System2Mai2026-3days_investigations.pdf`
📝 `kc7001_eastus_SolviSystems.kql`

**Certificate ID:** 55390 — May 2, 2026

Investigated a supply chain attack on an ICS/energy software provider.
Identified a failed XSS attack followed by a phishing campaign, malware
deployment (ecobug.exe), C2 communication, lateral movement across 38
machines, and data exfiltration.

**Key skills:** XSS detection · phishing campaign tracking · malware analysis · lateral movement · data exfiltration detection

---

### Investigation 3 — Whiskermania
📄 `kc7-certificate.pdf`

**Certificate ID:** 55592 — May 4, 2026

Completed Networking101 module. Investigated network activity at a cat
sanctuary, learning to navigate DNS events, HTTP status codes, and network
table structures.

**Key skills:** Network analysis · DNS investigation · table discovery · KQL `search *`

---

### Investigation 4 — Inside Encryptodera
📄 `kc7Inside_Encryptodera5daysinvesti4daymediumcertificate.pdf`
📄 `Encryptodera_Investigation_Report.pdf`
📝 `kc7001_eastus_Encryptodera.kql`

**Certificate ID:** 56329 — May 9, 2026

Investigated three concurrent threat campaigns at Encryptodera Financial:
- **Case 1 — Offensive Odor:** Insider data theft using 7-Zip and a USB drive
- **Case 2 — Crypto Conquest:** Ransomware encrypting 306 machines via Group Policy
- **Case 3 — Network Mystery:** Crypto wallet theft via FTP exfiltration over 27 days

**Key skills:** Insider threat detection · ransomware investigation · credential dumping (Mimikatz) · FTP exfiltration detection · multi-case incident reporting

---

## Learning Modules

| Module | Topics Covered | Certificate ID | Date |
| --- | --- | --- | --- |
| KQL 201 | Time analysis, aggregation, data transformation, advanced filtering | 55489 | May 3, 2026 |
| Decoding 101 | ROT13, XOR, Base64, Morse code, Pigpen cipher, Bacon cipher | — | May 2026 |

---

## KQL Files

| File | Investigation |
| --- | --- |
| `kc7001_eastus_Encryptodera.kql` | Inside Encryptodera |
| `kc7001_eastus_SolviSystems.kql` | Solvi Systems |

---

## Skills Demonstrated

- KQL advanced queries — `let` statements, `summarize`, `dcount`, `make_set`, `bin()`
- Phishing campaign tracking and email log analysis
- Election security and fraudulent domain detection
- XSS attack investigation and web log analysis
- ICS/supply chain attack investigation
- Insider threat detection and data exfiltration analysis
- Ransomware investigation — Group Policy mass deployment
- Crypto theft detection via FTP network flows
- Credential dumping detection (Mimikatz/LSASS)
- Cipher decoding — ROT13, XOR, Base64, Morse, Pigpen, Bacon
- Professional incident report writing

---

## Back to KC7 Overview

📁 [../README.md](../README.md)
