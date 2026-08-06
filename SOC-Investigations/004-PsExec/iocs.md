# Indicators of Compromise (IOCs)

## Network Indicators

| Type          | Value          | Description                     |
| ------------- | -------------- | ------------------------------- |
| Source IP     | `10.0.0.130`   | Initial attacker machine        |
| Target IP     | `10.0.0.133`   | First compromised host          |
| Target Host   | `sales-pc`     | Initial lateral movement target |
| Second Target | `marketing-PC` | Second pivot destination        |

---

## Authentication Indicators

| Type     | Value    |
| -------- | -------- |
| Username | `ssales` |
| Protocol | NTLMSSP  |

---

## PsExec Artifacts

| Artifact       | Description                                           |
| -------------- | ----------------------------------------------------- |
| `PSEXESVC.exe` | PsExec service executable deployed remotely           |
| `ADMIN$`       | Administrative share used for service installation    |
| `IPC$`         | SMB communication share used for remote communication |

---

## Network Protocols

| Protocol | Purpose                        |
| -------- | ------------------------------ |
| SMB      | File and service communication |
| SMB2     | PsExec activity detection      |
| NTLM     | Authentication analysis        |

