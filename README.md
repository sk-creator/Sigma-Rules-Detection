# Sigma Rules for SOC Detection

This repository contains Sigma rules authored to detect:

## 1. DNS Tunneling
- Detects abnormally long DNS queries (QueryLength > 100)
- Possible indicator of data exfiltration over DNS
- Maps to MITRE ATT&CK T1071.004

## 2. Lateral Movement with PsExec
- Detects use of PsExec for lateral movement
- Looks for EventID 4688 and PsExec in NewProcessName
- Maps to MITRE ATT&CK T1569.002

## Usage
- Use Sigma converters (sigmac) to transform these rules to SIEM queries.
- Compatible with Splunk, QRadar, ELK, etc.
