# 🛡️ Detection Queries

Collection of KQL detection queries developed for SOC monitoring and threat detection.

---

# Suspicious Failed Login Activity

## Objective

Identify accounts experiencing multiple failed authentication attempts.

```kql
SigninLogs
| where ResultType != 0
| summarize FailedAttempts=count() by UserPrincipalName, IPAddress
| where FailedAttempts > 5
| order by FailedAttempts desc
```

Detection Value:

- Brute force detection
- Password spraying investigation
- Account compromise analysis

---

# Suspicious Process Execution

## Objective

Identify unusual process activity.

```kql
DeviceProcessEvents
| where FileName in~ ("powershell.exe","cmd.exe","wscript.exe")
| project Timestamp, DeviceName, AccountName, FileName, ProcessCommandLine
```

Detection Value:

- Script execution monitoring
- Malware investigation
- Living-off-the-land detection

---

# Suspicious Network Connections

## Objective

Identify unusual outbound connections.

```kql
DeviceNetworkEvents
| where RemotePort !in (80,443)
| project Timestamp, DeviceName, RemoteIP, RemotePort, InitiatingProcessFileName
```

Detection Value:

- C2 discovery
- Malware communication
- Suspicious external traffic
