# Wazuh SIEM Lab – Endpoint Security

A hands-on Security Operations Center (SOC) project demonstrating the deployment of a **Wazuh SIEM Home Lab** for centralized endpoint monitoring, threat detection, and File Integrity Monitoring (FIM). The lab consists of an Ubuntu Server configured as the Wazuh Manager and a Windows endpoint registered as a monitored agent, providing real-time visibility into security events and endpoint activity. :contentReference[oaicite:0]{index=0}

---

# Project Overview

This project demonstrates the deployment of a **Wazuh SIEM Home Lab** for centralized endpoint monitoring and threat detection. Ubuntu Server was configured as the Wazuh Manager, while Windows acted as the monitored endpoint. The project includes secure agent registration, File Integrity Monitoring (FIM), and security event analysis through the Wazuh Dashboard. :contentReference[oaicite:0]{index=0}

---

# Objectives

- Deploy a Wazuh SIEM Home Lab
- Configure Ubuntu as the Wazuh Manager
- Register a Windows endpoint
- Verify secure communication between Manager and Agent
- Configure File Integrity Monitoring (FIM)
- Generate security events
- Analyze endpoint activity using the Wazuh Dashboard
- Gain practical experience in endpoint security monitoring

---

# Lab Environment

| Component | Details |
|-----------|---------|
| Virtualization Platform | VirtualBox |
| Wazuh Manager | Ubuntu Server 22.04 LTS |
| Endpoint | Windows 10 |
| Network | Bridged Adapter |
| SIEM Platform | Wazuh |
| Dashboard | Wazuh Dashboard |

:contentReference[oaicite:2]{index=2}

---

# Tools & Technologies

- Wazuh SIEM
- Ubuntu Server 22.04 LTS
- Windows 10
- VirtualBox
- Wazuh Dashboard
- Linux Terminal
- File Integrity Monitoring (FIM)

---

# Architecture

```text
                 Windows 10 Endpoint
                       │
                 Wazuh Agent
                       │
                Secure Registration
                       │
                       ▼
            Ubuntu Server 22.04 LTS
                Wazuh Manager
                       │
        ┌──────────────┼──────────────┐
        │              │              │
        ▼              ▼              ▼
   Log Collection   File Integrity   Security Events
     Monitoring      Monitoring        Dashboard
```

---

# Workflow

```text
Deploy Ubuntu Server
          │
          ▼
Install Wazuh Manager
          │
          ▼
Register Windows Agent
          │
          ▼
Verify Agent Connection
          │
          ▼
Configure File Integrity Monitoring
          │
          ▼
Generate File Events
          │
          ▼
Analyze Alerts
          │
          ▼
Monitor Security Events
```

---

# Implementation

## Step 1 – Create the Wazuh SIEM Lab

Created an Ubuntu Server virtual machine in VirtualBox, configured the network using a Bridged Adapter, verified internet connectivity, and updated the operating system before installing Wazuh. :contentReference[oaicite:3]{index=3}

### Screenshot

```
Screenshots/01_Lab_Setup.png
```

---

## Step 2 – Install Wazuh Manager

Installed the Wazuh Manager, Wazuh Indexer, and Wazuh Dashboard on Ubuntu. Registered a new Windows endpoint by creating an agent and generating the authentication key required for secure communication. :contentReference[oaicite:4]{index=4}

### Screenshot

```
Screenshots/02_Wazuh_Manager_Installation.png
```

---

## Step 3 – Configure the Windows Agent

Installed the Wazuh Windows Agent, configured the Manager IP address, imported the authentication key, and restarted the Wazuh service to establish communication with the Manager. :contentReference[oaicite:5]{index=5}

### Screenshot

```
Screenshots/03_Windows_Agent_Configuration.png
```

---

## Step 4 – Verify Agent Connection

Verified that the Windows endpoint successfully communicated with the Wazuh Manager by checking the registered agents from both the command line and the Wazuh Dashboard. The endpoint status was confirmed as **Active**. :contentReference[oaicite:6]{index=6}

### Screenshot

```
Screenshots/04_Agent_Connection_Status.png
```

---

## Step 5 – Configure File Integrity Monitoring (FIM)

Configured File Integrity Monitoring by modifying the `ossec.conf` configuration file to monitor a specific directory in real time. Restarted the Wazuh Agent to apply the configuration. :contentReference[oaicite:7]{index=7}

### Screenshot

```
Screenshots/05_FIM_Configuration.png
```

---

## Step 6 – Generate File Integrity Events

Performed file operations including file creation, modification, and deletion inside the monitored directory. Wazuh successfully detected each action and generated corresponding security alerts. :contentReference[oaicite:8]{index=8}

### Screenshot

```
Screenshots/06_File_Integrity_Alerts.png
```

---

## Step 7 – Analyze Security Events

Reviewed endpoint activity using the Wazuh Dashboard by filtering events based on the monitored agent, rule level, and event type. This provided centralized visibility into security events generated by the Windows endpoint. :contentReference[oaicite:9]{index=9}

### Screenshot

```
Screenshots/07_Security_Event_Analysis.png
```

---

## Step 8 – Generate Security Alerts

Triggered additional file events to validate the detection process. Confirmed that alerts appeared in the Wazuh Dashboard with their corresponding rule levels and descriptions, demonstrating successful end-to-end security monitoring. :contentReference[oaicite:10]{index=10}

### Screenshot

```
Screenshots/08_Security_Alerts.png
```

---

# Skills Demonstrated

- Wazuh SIEM Administration
- Ubuntu Server Administration
- Windows Endpoint Monitoring
- Agent Registration
- File Integrity Monitoring (FIM)
- Endpoint Security
- Security Event Analysis
- Threat Detection
- Log Analysis
- SOC Monitoring
- Incident Investigation

---

# Learning Outcomes

Through this project, I gained hands-on experience in:

- Deploying a Wazuh SIEM Home Lab
- Configuring Ubuntu as the Wazuh Manager
- Registering Windows endpoints securely
- Configuring File Integrity Monitoring (FIM)
- Monitoring endpoint security events
- Investigating alerts through the Wazuh Dashboard
- Understanding SIEM workflows and SOC operations
- Performing real-time endpoint monitoring

---

# Repository Structure

```text
Wazuh-SIEM-Lab/
│
├── README.md
├── Documentation/
│   └── Wazuh SIEM Lab.pdf
│
└── Screenshots/
    ├── 01_Lab_Setup.png
    ├── 02_Wazuh_Manager_Installation.png
    ├── 03_Windows_Agent_Configuration.png
    ├── 04_Agent_Connection_Status.png
    ├── 05_FIM_Configuration.png
    ├── 06_File_Integrity_Alerts.png
    ├── 07_Security_Event_Analysis.png
    └── 08_Security_Alerts.png
```

---

# Author

**VAISHNAVI MORE **

Cybersecurity Enthusiast | SOC Analyst | Blue Team | SIEM | Wazuh
