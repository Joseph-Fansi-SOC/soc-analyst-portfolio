# Investigation Timeline

| Step | Activity                                                             |
| ---- | -------------------------------------------------------------------- |
| 1    | Antivirus alerts detected suspicious behaviour after the 3CX update. |
| 2    | The MSI installer hash was analyzed using VirusTotal.                |
| 3    | Two malicious DLLs were identified.                                  |
| 4    | DLL Side-Loading was confirmed as the execution method.              |
| 5    | RC4-encrypted payload was observed during execution.                 |
| 6    | VMware detection indicated anti-analysis behaviour.                  |
| 7    | Threat intelligence linked the malware to the Lazarus Group.         |
| 8    | IOCs and MITRE ATT&CK techniques were documented.                    |

---

## Investigation Outcome

* Trojanized MSI installer identified.
* Two malicious DLLs recovered.
* RC4 encryption confirmed.
* DLL Side-Loading observed.
* Lazarus Group attribution identified.

