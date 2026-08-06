# 🚨 Detection Engineering Portfolio

This directory contains security detection rules, analytics logic, and defensive engineering exercises developed during my SOC analyst training.

The objective is to demonstrate the ability to transform security investigations and threat intelligence findings into actionable detections.

---

# 🎯 Skills Demonstrated

- Detection Engineering
- SIEM Rule Development
- Threat-Based Detection
- MITRE ATT&CK Mapping
- Log Analysis
- Alert Optimization
- False Positive Reduction

---

# 📂 Structure

## Sigma Rules

Location:

```
Sigma-Rules/
```

Contains platform-independent detection rules based on the Sigma standard.

Focus:

- Malware execution
- Suspicious PowerShell activity
- Credential access
- Persistence techniques
- Lateral movement

---

## Splunk Detections

Location:

```
Splunk-Detections/
```

Contains SPL-based detection searches.

Examples:

- Suspicious authentication
- Malware indicators
- Network anomalies
- Endpoint activity

---

## Wazuh Rules

Location:

```
Wazuh-Rules/
```

Contains custom Wazuh detection logic.

Examples:

- Windows event monitoring
- File integrity monitoring
- Suspicious command execution
- Security alert enrichment

---

# 🔍 Detection Development Methodology

Each detection follows this process:

## 1. Threat Understanding

Identify:

- Threat behavior
- Attack technique
- Indicators
- Required telemetry

---

## 2. Detection Logic

Define:

- Data source
- Query logic
- Detection conditions
- Severity

---

## 3. Validation

Test against:

- Lab activity
- Simulated attacks
- Security datasets

---

## 4. Documentation

Record:

- Detection purpose
- MITRE ATT&CK mapping
- Investigation steps
- Response recommendations

---

# 🛠️ Technologies

- Splunk
- Wazuh
- Sigma
- MITRE ATT&CK
- Windows Event Logs
- Sysmon
- KQL concepts

---

# 🚀 Objective

Develop practical detection capabilities required for SOC Analyst and Detection Engineer roles.
