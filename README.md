🛡 Enterprise SOC Homelab – Wazuh SIEM Detection Lab
📌 Project Overview

This project demonstrates the design and implementation of a Security Operations Center (SOC) homelab using Wazuh SIEM, Sysmon, and controlled attack simulations from Kali Linux.

The objective was to simulate real-world adversary techniques and validate detection capabilities using log ingestion, correlation, and MITRE ATT&CK mapping.

This lab replicates practical SOC analyst responsibilities including log analysis, alert validation, attack detection, and detection engineering.

-------------------------------------------------------------------------------------------------------------------------------------------------
🏗 Lab Architecture
💻 Virtual Environment (VirtualBox)
Machine	Role	OS
Ubuntu Server	Wazuh Manager	Ubuntu
Windows 10	Victim / Log Source	Windows 10
Kali Linux	Attacker	Kali Linux
--------------------------------------------------------------------------------------------------------------------------------------------------

🌐 Network Configuration

Host-Only Adapter for internal communication

NAT (Ubuntu only) for updates

All systems validated via ping testing

Agent communication verified using agent_control

----------------------------------------------------------------------------------------------------------------------------------------------------
🛠 Technologies Used

Wazuh SIEM

Windows Event Logging

Sysmon (System Monitor)

Kali Linux (Hydra, PowerShell payloads)

MITRE ATT&CK Framework

VirtualBox

PowerShell

Linux CLI

------------------------------------------------------------------------------------------------------------------------------------------------------
🚨 Attack Simulations Performed
1️⃣ RDP Brute Force Attack

Tool Used: Hydra
Target: Windows 10
Technique: Credential brute force

🔎 Detection:

Windows Event ID 4625 (Failed Logon)

Wazuh Rule ID: 60122

MITRE ATT&CK:

T1110 – Brute Force

T1531 – Account Access Removal

📊 Result:

Multiple authentication failure alerts generated and visualized in Wazuh dashboard.

------------------------------------------------------------------------------------------------------------------------------------------------------------
2️⃣ PowerShell Encoded Command Execution

Technique: Base64-encoded PowerShell execution
Objective: Simulate malicious script execution

🔎 Detection:

Wazuh Rule ID: 92057

Severity Level: 12 (High)

MITRE ATT&CK:

T1059.001 – PowerShell Execution

📊 Result:

High-severity alert triggered indicating execution of encoded PowerShell command.

This demonstrates detection of obfuscated attack behavior.

---------------------------------------------------------------------------------------------------------------------------------------------------------------
3️⃣ Account Discovery Activity

Technique: net.exe account enumeration

🔎 Detection:

Wazuh Rule ID: 92039

MITRE ATT&CK:

T1087 – Account Discovery

📊 Result:

Discovery activity logged and successfully detected.

🧠 Detection Engineering

Enhancements implemented:

Installed Sysmon for enhanced Windows telemetry

Enabled process creation & command-line auditing

Validated log ingestion using alerts.json

Created custom detection rules for suspicious network ports

Mapped alerts to MITRE ATT&CK techniques
-----------------------------------------------------------------------------------------------------------------------------------------------------------
📈 SOC Analyst Skills Demonstrated

SIEM deployment and configuration

Windows log auditing and analysis

Sysmon integration

Attack simulation & validation

Alert triage and severity analysis

MITRE ATT&CK mapping

Troubleshooting log ingestion issues

Network troubleshooting in virtual environments

Incident documentation

🔎 Example Detections Observed

PowerShell spawning PowerShell with encoded command

Logon failure – Unknown user or bad password

Account discovery commands executed

Suspicious parent-child process relationships

----------------------------------------------------------------------------------------------------------------------------------------
Repository Structure
SOC-Homelab-Wazuh-Detection-Lab/
│
├── Architecture/
├── Environment-Setup/
├── Attack-Simulation/
├── Detection-Engineering/
├── Incident-Reports/
├── Screenshots/
└── README.md
-----------------------------------------------------------------------------------------------------------------------------------------
Key Learning Outcomes

Understanding log pipelines from endpoint to SIEM

Detecting adversary techniques using telemetry

Configuring secure lab networking

Handling endpoint security interference (Defender)

Validating alerts using real attack scenarios

Translating technical findings into SOC documentation

-------------------------------------------------------------------------------------------------------------------------------------------
🚀 Future Improvements

Add Sigma rule integration

Implement automated alert correlation

Simulate lateral movement

Integrate threat intelligence feeds

Create custom dashboards for specific attack types

------------------------------------------------------------------------------------------------------------------------------------------------
📌 Conclusion

This project demonstrates hands-on SOC analyst capability including:

Detection validation

Attack simulation

SIEM configuration

Threat mapping using MITRE ATT&CK

Alert investigation

The lab replicates real-world SOC workflows and reflects practical defensive security experience beyond theoretical knowledge.


Author

VINOD BALLA
Final Year Student | Aspiring SOC Analyst
Open to SOC L1 / Cybersecurity Internship Opportunities



