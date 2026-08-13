# Real-Time PowerShell Monitoring using Splunk Enterprise

A hands-on Security Operations Center (SOC) project demonstrating the collection, monitoring, and analysis of Windows PowerShell Operational logs using **Splunk Enterprise** and the **Splunk Universal Forwarder**. This project focuses on detecting suspicious PowerShell activity through Search Processing Language (SPL) queries, dashboards, and real-time alerts to simulate real-world SOC monitoring and threat detection. :contentReference[oaicite:0]{index=0}

---

# Project Overview

PowerShell is one of the most commonly abused tools by attackers due to its powerful automation and scripting capabilities. Monitoring PowerShell activity is essential for detecting malicious behavior such as encoded commands, payload downloads, and script execution.

In this project, Windows PowerShell Operational Logging was enabled and integrated with Splunk Enterprise. Logs were collected in real time using Splunk Universal Forwarder, analyzed with SPL queries, and visualized through dashboards. Real-time alerts were also configured to automatically detect suspicious PowerShell activity. :contentReference[oaicite:1]{index=1}

---

# Objectives

- Install and configure Splunk Enterprise
- Configure Splunk Universal Forwarder
- Enable Windows PowerShell Operational Logging
- Collect PowerShell logs in real time
- Analyze Event ID 4104
- Detect suspicious PowerShell commands using SPL
- Build dashboards for monitoring
- Configure real-time alerts

---

# Lab Environment

| Component | Details |
|-----------|---------|
| Operating System | Windows 11 |
| SIEM Platform | Splunk Enterprise |
| Log Forwarder | Splunk Universal Forwarder |
| Log Source | Windows PowerShell Operational Logs |
| Query Language | SPL |
| Environment | Local Host |

:contentReference[oaicite:2]{index=2}

---

# Tools & Technologies

- Splunk Enterprise
- Splunk Universal Forwarder
- Windows 11
- Windows PowerShell
- Windows Event Viewer
- Search Processing Language (SPL)

---

# Project Architecture

```text
Windows 11
      │
      │
PowerShell Operational Logs
      │
      ▼
Splunk Universal Forwarder
      │
      ▼
Splunk Enterprise
      │
      ├── Log Collection
      ├── SPL Queries
      ├── Threat Detection
      ├── Dashboards
      └── Real-Time Alerts
```

---

# Workflow

```text
Enable PowerShell Operational Logging
                │
                ▼
Generate PowerShell Events
                │
                ▼
Collect Windows Event Logs
                │
                ▼
Forward Logs to Splunk
                │
                ▼
Search & Analyze using SPL
                │
                ▼
Detect Suspicious Activity
                │
                ▼
Create Dashboards
                │
                ▼
Generate Real-Time Alerts
```

---

# Implementation

## Step 1 – Install and Configure Splunk Enterprise

Splunk Enterprise was installed and configured to receive Windows Event Logs. The administrator account was created, and the Splunk Web interface was verified before beginning log collection. :contentReference[oaicite:3]{index=3}

### Screenshot

<img width="1381" height="653" alt="01_PowerShell_Operational_Logs_Overview png" src="https://github.com/user-attachments/assets/fa2de9ef-915e-4351-8eb2-35a9b029b82c" />


---

## Step 2 – Configure Splunk Universal Forwarder

The Splunk Universal Forwarder was configured to securely forward Windows PowerShell Operational logs to Splunk Enterprise.

Tasks performed:

- Verified Forwarder service
- Connected Forwarder to Splunk
- Restarted the service
- Verified successful communication

:contentReference[oaicite:4]{index=4}

> *(No screenshot available for this step.)*

---

## Step 3 – Enable PowerShell Operational Logging

PowerShell Operational Logging was enabled to capture PowerShell execution events. Several PowerShell commands were executed to generate test events before verifying that logs were successfully indexed inside Splunk.

**Important Event**

- Event ID **4104** (PowerShell Script Block Logging)

:contentReference[oaicite:5]{index=5}

### Screenshot

<img width="841" height="262" alt="03_Test_Event_Generation_PowerShell png" src="https://github.com/user-attachments/assets/48921d8f-957e-45a1-b3c0-2f88356a108e" />

---

## Step 4 – Analyze PowerShell Logs using SPL

PowerShell Operational logs were analyzed using SPL queries.

The detection rule searched for commonly abused PowerShell keywords:

- EncodedCommand
- DownloadString
- Invoke-Expression

The generated test event successfully matched the detection query.

:contentReference[oaicite:6]{index=6}

### Screenshot 1

<img width="1381" height="653" alt="01_PowerShell_Operational_Logs_Overview png" src="https://github.com/user-attachments/assets/c688bc5e-1019-4d0c-b619-131b38c8efa4" />

### Screenshot 2

<img width="1381" height="648" alt="02_Suspicious_PowerShell_Command_Detection png" src="https://github.com/user-attachments/assets/09611789-7479-44d7-b01b-b9a448970051" />

### Screenshot 3

<img width="841" height="262" alt="03_Test_Event_Generation_PowerShell png" src="https://github.com/user-attachments/assets/3050a50c-539f-484b-8aa3-a2f38f1757b3" />


---

## Step 5 – Dashboard & Real-Time Alert Configuration

Security dashboards were created to visualize PowerShell activity over time. A real-time alert was configured to automatically notify whenever suspicious PowerShell commands matching the detection rule were executed.

Alert Configuration

- Alert Type: Real-Time
- Trigger: Per Result
- Alert Name: Suspicious PowerShell Activity

:contentReference[oaicite:7]{index=7}

> **Note:** The dashboard and alert configuration screenshots can be added later if available.


# Detection Logic

The detection query identifies PowerShell script block events (Event ID 4104) containing keywords frequently associated with malicious activity.

```spl
index=main sourcetype="WinEventLog:Microsoft-Windows-PowerShell/Operational" EventCode=4104
("EncodedCommand" OR "DownloadString" OR "Invoke-Expression")
```

---

# Skills Demonstrated

- SIEM Administration
- Splunk Enterprise
- Splunk Universal Forwarder
- Windows Event Log Analysis
- Windows PowerShell Monitoring
- Event ID 4104 Investigation
- SPL Query Development
- Threat Detection
- Dashboard Development
- Alert Engineering
- SOC Monitoring
- Incident Investigation

---

# Learning Outcomes

Through this project, I gained hands-on experience in:

- Deploying Splunk Enterprise
- Configuring Universal Forwarder
- Monitoring Windows PowerShell Operational Logs
- Investigating Event ID 4104
- Writing SPL detection queries
- Detecting suspicious PowerShell execution
- Building dashboards
- Creating real-time alerts
- Applying SOC investigation techniques

---

# Repository Structure

```text
Real-Time-PowerShell-Monitoring/
│
├── README.md
├── Documentation/
│   └── Real-Time PowerShell Monitoring.pdf
│
└── Screenshots/
    ├── 01_PowerShell_Operational_Logs_Overview.png
    ├── 02_Suspicious_PowerShell_Command_Detection.png
    ├── 03_Test_Event_Generation_PowerShell.png
    ├── 04_Detection_Query_Results.png
    └── 05_Event_ID_4104_Details.png
```

---

# Author

**VAISHNAVI MORE **

Cybersecurity Enthusiast | SOC Analyst | Blue Team | SIEM | Splunk
