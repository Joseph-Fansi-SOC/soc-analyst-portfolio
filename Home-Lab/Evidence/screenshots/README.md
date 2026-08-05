## Home Lab — Screenshots

### Wazuh Vulnerability Assessment
**File:** wazuh-vulnerability-scan.png (or your filename)

Real-world investigation of a friend's PC (Project 05).
Wazuh identified 13 vulnerabilities including 1 Critical
and 4 High severity CVEs on Windows 10 Pro.

Key findings:
- CVE-2022-31901, CVE-2022-31902, CVE-2022-41325
- CVE-2023-38538, CVE-2023-40031
- Vulnerable software: Notepad++, VLC, WhatsApp

---

### Wireshark Network Analysis
**File:** wireshark-capture.png (or your filename)

Captured live network traffic on Ubuntu (enp0s3 interface)
during friend's PC investigation.

Key findings:
- TLSv1.3 encrypted traffic detected
- SNI identified: cti.wazuh.com (Wazuh cloud telemetry)
- TCP handshake analysis — SYN/ACK sequences captured
- Confirmed Wazuh agent communicating with cloud server

Tools: Wireshark on Ubuntu 24.04 (sudo wireshark)
Interface: enp0s3 (ethernet)

