# 🗺️ MITRE ATT&CK Mapping Portfolio

This directory contains MITRE ATT&CK mappings created from security investigations, threat hunting exercises, malware analysis, and SOC lab activities.

The objective is to demonstrate the ability to translate attacker behavior into standardized adversary techniques.

---

# 🎯 Skills Demonstrated

- MITRE ATT&CK framework usage
- Threat behavior analysis
- Incident investigation
- Detection engineering
- Threat intelligence analysis
- Adversary emulation concepts

---

# 📂 Contents

## ATT&CK Matrix

Location:

```
ATT&CK-Matrix.md
```

Reference guide of commonly observed attacker techniques.

---

## SOC Investigation Mappings

Location:

```
SOC-Investigation-Mappings.md
```

Contains MITRE mappings from completed investigations:

Examples:

- 3CX Supply Chain Attack
- Yellow RAT
- PsExec Lateral Movement
- Red Stealer
- WebStrike Web Shell

---

## Threat Technique Reference

Location:

```
Threat-Technique-Reference.md
```

Quick analyst reference for common techniques.

---

# 🔍 Investigation Mapping Methodology

Each investigation is mapped using:

## 1. Attack Behavior

Example:

```
Malware loads malicious DLL
```

---

## 2. MITRE Technique

Example:

```
T1574.002
DLL Side-Loading
```

---

## 3. Evidence

Example:

```
ffmpeg.dll loaded by legitimate 3CX.exe
```

---

## 4. Detection Opportunity

Example:

```
Monitor unusual DLL loading from application directories
```

---

# 🛠️ Framework

Primary framework:

- MITRE ATT&CK Enterprise

Used for:

- Threat intelligence
- Detection engineering
- Incident reporting
- SOC investigations

---

# 🚀 Objective

Develop the ability to understand attacker behavior and convert investigations into actionable defensive controls.
