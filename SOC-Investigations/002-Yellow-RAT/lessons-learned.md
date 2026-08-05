# Lessons Learned

## Key Takeaways

* Malware analysis should always be performed in an isolated environment.
* Hash analysis and threat intelligence platforms provide valuable context during triage.
* RAT malware can provide attackers with persistent remote access.
* Network indicators are critical for identifying and blocking C2 communication.

---

## Detection Opportunities

* Monitor suspicious DLL execution from user directories.
* Hunt for unexpected files in:

```
%USERPROFILE%\AppData\Roaming\
```

* Block known malicious domains.
* Monitor unusual outbound connections from endpoints.
* Investigate browser redirection behavior as a possible malware indicator.

---

## Defensive Recommendations

* Maintain endpoint detection capabilities.
* Use application control policies.
* Monitor persistence locations.
* Regularly update threat intelligence feeds.
* Perform proactive IOC hunting.

---

## Skills Demonstrated

* Malware Triage
* Threat Intelligence
* IOC Extraction
* C2 Analysis
* Incident Response Documentation
* Secure Malware Handling

---

## AI Assistance

AI was used to improve documentation structure, organize findings, and review technical descriptions.

The malware investigation, evidence review, IOC validation, and conclusions were independently performed by the analyst.

