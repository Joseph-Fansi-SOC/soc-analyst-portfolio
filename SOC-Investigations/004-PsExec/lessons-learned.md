# Lessons Learned

## Key Takeaways

* Network traffic can reveal attacker movement even without endpoint logs.
* SMB analysis is critical for detecting Windows lateral movement.
* PsExec is a legitimate administration tool that can be abused by attackers.
* Administrative shares provide valuable forensic evidence.

---

## Detection Opportunities

Monitor for:

* Unexpected SMB connections.
* Remote service creation.
* PsExec artifacts (`PSEXESVC.exe`).
* ADMIN$ and IPC$ access from unusual hosts.
* NTLM authentication anomalies.

---

## Defensive Recommendations

* Reduce unnecessary administrative share exposure.
* Monitor privileged account usage.
* Implement strong authentication controls.
* Collect endpoint and network telemetry together.
* Hunt for MITRE ATT&CK techniques:

  * T1021.002
  * T1569.002
  * T1078

---

## Additional Analyst Work

During this investigation, additional effort was invested in developing a personal Wireshark analysis reference guide:

**Wireshark Analyst Bible**

* 200+ filters
* 15 analysis categories
* SOC-focused investigation workflow

This resource was created to improve repeatability during future PCAP investigations.

---

## AI Assistance

AI was used to assist with documentation organization, technical wording, and structuring investigation outputs.

All Wireshark analysis, packet investigation, filtering methodology, and conclusions were independently performed by the analyst.

