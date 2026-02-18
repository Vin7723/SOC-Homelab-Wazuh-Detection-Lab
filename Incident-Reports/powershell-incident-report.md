# Incident Report – Suspicious PowerShell Execution

## Incident Summary
A high-severity alert was generated indicating execution of a base64 encoded PowerShell command.

## Detection Details
- Rule ID: 92057
- Severity: 12 (High)
- MITRE ATT&CK: T1059.001 – PowerShell Execution

## Timeline
- PowerShell process spawned
- Encoded command executed
- Alert triggered in Wazuh dashboard

## Analysis
The activity indicates possible command obfuscation commonly used in malware or reverse shell attempts.

## Impact
Potential unauthorized command execution.

## Remediation
- Investigate parent process
- Validate command contents
- Isolate affected system if malicious

## Lessons Learned
Encoded PowerShell commands are strong indicators of malicious activity and should be monitored closely.
