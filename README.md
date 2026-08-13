# SOC Projects

A collection of hands-on Security Operations Center (SOC) projects demonstrating practical experience in SIEM deployment, log collection, threat detection, security monitoring, and incident investigation using industry-standard tools.

These projects were built in isolated lab environments to simulate real-world SOC workflows, focusing on log analysis, endpoint monitoring, dashboard creation, alert engineering, and threat detection.

---

## Skills Demonstrated

- Security Information and Event Management (SIEM)
- Splunk Enterprise Administration
- Wazuh SIEM
- Windows Event Log Analysis
- PowerShell Monitoring
- Authentication Log Investigation
- File Integrity Monitoring (FIM)
- Endpoint Security
- Security Dashboard Development
- Real-Time Alerting
- SPL (Search Processing Language)
- Linux Administration
- Windows Administration
- Bash
- AWK
- Incident Investigation
- Threat Detection

---

## Tools & Technologies

- Splunk Enterprise
- Splunk Universal Forwarder
- Wazuh SIEM
- Ubuntu Linux
- Windows 10 / Windows 11
- PowerShell
- Bash
- AWK
- Windows Event Viewer
- VirtualBox
- Search Processing Language (SPL)

---

# Projects

## 1. Real-Time PowerShell Monitoring

**Tools**

Splunk Enterprise • Universal Forwarder • Windows 11 • PowerShell • SPL

### Overview

Designed and deployed a real-time PowerShell monitoring solution by forwarding Windows PowerShell Operational logs into Splunk Enterprise.

Implemented PowerShell Operational Logging, analyzed Event ID 4104, developed SPL detection queries, built dashboards, and configured real-time alerts for suspicious PowerShell execution.

### Skills

- Windows Event Logs
- Splunk Enterprise
- SPL
- Alert Engineering
- Dashboard Creation
- Threat Detection

📁 Folder

```
Real-Time-PowerShell-Monitoring/
```

---

## 2. Wazuh SIEM Lab – Endpoint Security

**Tools**

Wazuh SIEM • Ubuntu Server • Windows • VirtualBox • File Integrity Monitoring

### Overview

Built a complete Wazuh SIEM home lab with Ubuntu acting as the Wazuh Manager and Windows configured as the monitored endpoint.

Configured secure agent registration, centralized log collection, File Integrity Monitoring (FIM), and investigated endpoint security events through the Wazuh Dashboard.

### Skills

- Wazuh SIEM
- Endpoint Monitoring
- File Integrity Monitoring
- Linux Administration
- Windows Security

📁 Folder

```
Wazuh-SIEM-Lab/
```

---

## 3. Windows Failed Login Detection & SIEM Monitoring

**Tools**

Splunk Enterprise • Ubuntu Linux • Windows • AWK • Bash • SPL

### Overview

Generated Windows Security Event ID 4625 logs, parsed exported security logs using AWK, transferred them into Splunk Enterprise, and investigated failed authentication attempts.

Built SPL searches and dashboards to identify suspicious login behavior, source IP addresses, and targeted user accounts.

### Skills

- Windows Security Logs
- Event ID 4625
- Splunk
- SPL
- AWK
- Bash
- Authentication Analysis

📁 Folder

```
Windows-Failed-Login-Detection/
```

---

# Repository Structure

```
SOC-Projects/
│
├── README.md
│
├── Real-Time-PowerShell-Monitoring/
│   ├── README.md
│   ├── Documentation/
│   └── Screenshots/
│
├── Wazuh-SIEM-Lab/
│   ├── README.md
│   ├── Documentation/
│   └── Screenshots/
│
└── Windows-Failed-Login-Detection/
    ├── README.md
    ├── Documentation/
    └── Screenshots/
```

---

# Learning Outcomes

Through these projects, I gained hands-on experience in:

- SIEM deployment and configuration
- Windows Event Log monitoring
- Endpoint security monitoring
- Security log analysis
- Threat detection
- Dashboard creation
- Alert engineering
- SPL query development
- Incident investigation
- Authentication analysis
- PowerShell monitoring
- File Integrity Monitoring (FIM)

---

## Author

**Shivam Pandey**

Cybersecurity Enthusiast | SOC Analyst | Blue Team
