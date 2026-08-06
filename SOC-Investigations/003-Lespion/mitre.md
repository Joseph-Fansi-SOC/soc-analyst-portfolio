# MITRE ATT&CK Mapping

| Tactic               | Technique                        | ID    | Evidence                                              |
| -------------------- | -------------------------------- | ----- | ----------------------------------------------------- |
| Initial Access       | Valid Accounts                   | T1078 | Exposed credentials could enable unauthorized access. |
| Credential Access    | Credentials from Password Stores | T1555 | Sensitive authentication data discovered.             |
| Credential Access    | Unsecured Credentials            | T1552 | Secrets exposed in GitHub repositories.               |
| Discovery            | Search Open Websites/Domains     | T1593 | OSINT investigation using public sources.             |
| Resource Development | Obtain Capabilities              | T1588 | API keys and online resources identified.             |
| Impact               | Resource Hijacking               | T1496 | XMRig cryptocurrency mining activity identified.      |

---

## Observed Attack Techniques

### Unsecured Credentials (T1552)

Sensitive authentication information was exposed through public GitHub repositories.

### Search Open Websites/Domains (T1593)

Open-source intelligence techniques were used to correlate online identities and discover additional information.

### Resource Hijacking (T1496)

Cryptocurrency mining activity was linked to the use of XMRig.

