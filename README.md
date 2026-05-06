# Wazuh SIEM Home Lab — Authentication Monitoring and Privilege Escalation Detection

## Overview

This project demonstrates the deployment and configuration of a Wazuh SIEM home lab used for detecting authentication abuse, password guessing attempts, and privilege escalation activity on a Linux endpoint.

The environment was built using Kali Linux as a monitored endpoint connected to a Wazuh manager. Multiple attack simulations were performed to generate real security telemetry and validate Wazuh detection capabilities.

---

# Technologies Used

- Wazuh
- Kali Linux
- Linux PAM
- SSH
- Syslog
- MITRE ATT&CK
- PCI DSS

---

# Objectives

- Detect failed authentication attempts
- Monitor password guessing activity
- Detect sudo abuse and privilege escalation
- Analyze Linux authentication telemetry
- Validate MITRE ATT&CK mappings
- Validate PCI DSS mappings

---

# Attack Simulation

The following simulations were performed:

1. Failed sudo authentication attempts
2. Password guessing attempts
3. SSH authentication failures
4. Successful privilege escalation using sudo

---

# Detection Results

## Important Wazuh Rules

| Rule ID | Description |
|---|---|
| 5557 | unix_chkpwd: Password check failed |
| 5503 | PAM: User login failed |
| 5760 | sshd: authentication failed |
| 5404 | Three failed attempts to run sudo |
| 5402 | Successful sudo to ROOT executed |

---

# MITRE ATT&CK Mapping

| Technique ID | Technique |
|---|---|
| T1110.001 | Password Guessing |
| T1548.003 | Sudo and Sudo Caching |
| T1078 | Valid Accounts |
| T1021 | Remote Services |

---

# Skills Demonstrated

- SIEM deployment
- Wazuh administration
- Linux security monitoring
- Authentication log analysis
- MITRE ATT&CK analysis
- Alert correlation
- Privilege escalation detection
- SOC alert investigation
- Blue Team operations

---

# Repository Structure

```text
wazuh-authentication-monitoring-lab/
│
├── README.md
├── report/
│   └── wazuh_detection_report.docx
│
├── screenshots/
│   ├── agent-connected.png
│   ├── failed-sudo.png
│   ├── password-guessing.png
│   ├── mitre-mapping.png
│   ├── pci-dss-events.png
│   └── successful-root.png
│
├── configs/
│   └── ossec.conf
│
└── logs/
    └── sample-alerts.txt
```

---

# Conclusion

This lab demonstrated how Wazuh SIEM can be used to monitor Linux authentication activity, detect password guessing attacks, and identify privilege escalation attempts.

The project demonstrates practical SOC analyst and Blue Team skills related to:

- SIEM operations
- Alert investigation
- Security telemetry analysis
- MITRE ATT&CK mapping
- Linux security monitoring
