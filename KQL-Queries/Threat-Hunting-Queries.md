# 🔍 Threat Hunting Queries

Proactive hunting queries designed to identify attacker behavior.

---

# PowerShell Abuse Hunting

MITRE ATT&CK:

```
T1059.001 - PowerShell
```

Query:

```kql
DeviceProcessEvents
| where FileName =~ "powershell.exe"
| where ProcessCommandLine contains "-enc"
| project Timestamp, DeviceName, AccountName, ProcessCommandLine
```

Purpose:

Detect encoded PowerShell execution.

---

# Possible Credential Access Activity

MITRE ATT&CK:

```
T1003 - OS Credential Dumping
```

Query:

```kql
DeviceProcessEvents
| where ProcessCommandLine contains "lsass"
| project Timestamp, DeviceName, ProcessCommandLine
```

Purpose:

Identify suspicious LSASS access attempts.

---

# Lateral Movement Hunting

MITRE ATT&CK:

```
T1021 - Remote Services
```

Query:

```kql
DeviceLogonEvents
| where LogonType contains "Remote"
| project Timestamp, DeviceName, AccountName, RemoteIP
```

Purpose:

Identify suspicious remote authentication activity.
