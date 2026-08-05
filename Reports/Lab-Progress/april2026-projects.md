## Home Lab — Projects & Real-World Cases April 2026

---

### Project 01 — Build SOC Lab: SIEM (Wazuh) with AI support
**Category:** Lab Project
**Duration:** 9 days

Built a personal SOC environment using Wazuh as SIEM
with AI support for basic investigations.

---

### Project 02 — Build SIEM Lab with Wazuh + Splunk
**Category:** Lab Project
**Duration:** 9 days

Extended the lab by integrating Splunk alongside Wazuh
for dual-SIEM visibility and log correlation.

---

### Project 03 — Install Ubuntu in VirtualBox
**Category:** Lab Project
**Duration:** 2 days

Set up Ubuntu 24.04 in VirtualBox as the base environment
for all home lab tools.

---

### Project 04 — Install Wireshark on Ubuntu 24.04
**Category:** Lab Project
**Duration:** 1 day

Installed and configured Wireshark on Ubuntu for
network packet capture and analysis.

---

### Project 05 — Friend's PC Investigation with Wazuh
**Category:** Real-World Case ⭐
**Duration:** 4 days

**Scenario:** Friend reported suspected spoofing,
memory overflow and high CPU/fan activity.

**Tools used:** Wazuh

**Investigation steps:**
- Ingested endpoint logs into Wazuh
- Analysed alerts for suspicious processes
- Investigated memory and CPU anomalies
- Checked for indicators of spoofing activity

**Outcome:**
Wazuh vulnerability scan revealed 13 findings:
- 1 Critical severity
- 4 High severity
- 8 Medium severity

**CVEs identified:**
| CVE | Severity |
|-----|----------|
| CVE-2022-31901 | High |
| CVE-2022-31902 | High |
| CVE-2022-41325 | High |
| CVE-2023-38538 | High |
| CVE-2023-40031 | High |

**Vulnerable software found:**
- Notepad++ 32-bit x86 — 7 vulnerabilities
- VLC media player — 4 vulnerabilities
- WhatsApp — 2 vulnerabilities

**Recommendations given to friend:**
- Immediately update Notepad++, VLC and WhatsApp
- Enable Windows Update
- Remove unused software
- Run regular Wazuh scans

---

### Skills demonstrated
- Wazuh installation and administration
- Splunk + Wazuh integration
- VirtualBox environment setup
- Wireshark installation on Linux
- Real-world endpoint investigation
- Incident report writing

