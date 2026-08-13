# SOC Failed Login Detection & SIEM Monitoring

A hands-on Security Operations Center (SOC) project demonstrating the detection and investigation of **Windows Failed Login Events (Event ID 4625)** using **Splunk Enterprise**, **Ubuntu Linux**, **AWK**, and **Bash**. The project covers log collection, parsing, ingestion into Splunk, and visualization of authentication failures through dashboards.

---

# Project Overview

This project demonstrates how Windows failed login events (Event ID 4625) can be exported, processed on Ubuntu using AWK, imported into Splunk Enterprise, and analyzed to identify suspicious authentication activity.

---

# Objectives

- Generate Windows failed login events
- Export Windows Security Logs
- Parse logs using AWK
- Transfer processed logs to Windows
- Import logs into Splunk Enterprise
- Analyze failed login events using SPL
- Build visualizations for SOC monitoring

---

# Lab Environment

| Component | Details |
|----------|---------|
| SIEM Platform | Splunk Enterprise |
| Operating Systems | Windows 10 & Ubuntu Linux |
| Scripting | Bash, AWK |
| Log Source | Windows Security Logs |
| Event ID | 4625 (Failed Login) |
| Data Format | CSV |

---

# Tools & Technologies

- Splunk Enterprise
- Ubuntu Linux
- Windows Security Event Logs
- Bash
- AWK
- Python HTTP Server
- Search Processing Language (SPL)

---

# Architecture

```text
Windows Security Logs
        │
Generate Failed Login Events
        │
        ▼
Export CSV
        │
        ▼
Ubuntu Linux
        │
Parse Logs using AWK
        │
        ▼
Transfer CSV
        │
        ▼
Splunk Enterprise
        │
        ├── Search
        ├── Log Analysis
        ├── Visualization
        └── SOC Investigation
```

---

# Workflow

```text
Generate Failed Logins
        │
        ▼
Export Security Logs
        │
        ▼
Parse CSV using AWK
        │
        ▼
Transfer CSV to Windows
        │
        ▼
Import into Splunk
        │
        ▼
Analyze using SPL
        │
        ▼
Create Visualizations
```

---

# Implementation

## Step 1 – Generate Failed Login Events

Generated multiple failed login attempts using incorrect credentials on Windows. These events were recorded as **Event ID 4625** in the Windows Security Log.

> **Screenshot**
<img width="1378" height="609" alt="01_CSV_Data_Import_Success png" src="https://github.com/user-attachments/assets/49c8a598-f16d-4cb5-bafc-8d7159f0ff10" />


---

## Step 2 – Parse Security Logs using AWK

Exported the Windows Security Logs to Ubuntu Linux and used AWK commands to filter and process failed login records before importing them into Splunk.

> **Screenshot**
<img width="1378" height="677" alt="02_Imported_Failed_Login_Events png" src="https://github.com/user-attachments/assets/8e7cf1ce-ac5c-4e70-89be-66e2c9d167b1" />


---

## Step 3 – Import CSV into Splunk Enterprise

Transferred the processed CSV file from Ubuntu to Windows and imported it into Splunk Enterprise. Verified that the log file was successfully indexed.

> **Screenshot**
<img width="1378" height="609" alt="01_CSV_Data_Import_Success png" src="https://github.com/user-attachments/assets/8faf92b8-4486-4aec-8cc2-ca96c57016d3" />


---

## Step 4 – Verify Imported Log Events

Searched the imported CSV source in Splunk to confirm that all failed login events were successfully ingested.

> **Screenshot**
<img width="1378" height="677" alt="02_Imported_Failed_Login_Events png" src="https://github.com/user-attachments/assets/02733868-61f2-4d81-96fc-f65d6072ab51" />


---

## Step 5 – Analyze Raw Log Data

Viewed the imported records in the **Statistics** tab to inspect the raw authentication data before creating visualizations.

> **Screenshot**
<img width="1378" height="663" alt="03_Failed_Login_Raw_Log_Analysis png" src="https://github.com/user-attachments/assets/3a9c8491-8f5c-469b-92c8-541c44f8667c" />


---

## Step 6 – Create Event Timeline

Created a **timechart** visualization in Splunk to monitor failed login attempts over time, helping identify spikes in authentication failures.

> **Screenshot**
<img width="1378" height="656" alt="04_Failed_Login_Event_Timeline png" src="https://github.com/user-attachments/assets/95812e09-4e17-4c0c-97b6-cc363645bd1a" />

---

# Sample SPL Queries

### View Imported Logs

```spl
source="failed_logins_detailed.csv"
```

### Display Raw Log Table

```spl
source="failed_logins_detailed.csv"
| table _raw
```

### Count Events Over Time

```spl
source="failed_logins_detailed.csv"
| timechart count
```

---

# Skills Demonstrated

- Splunk Enterprise
- Windows Security Log Analysis
- Event ID 4625 Investigation
- Linux Administration
- AWK Log Parsing
- Bash Scripting
- CSV Log Processing
- SPL Query Development
- Dashboard & Visualization
- SOC Monitoring
- Authentication Analysis

---

# Learning Outcomes

After completing this project, I gained hands-on experience in:

- Investigating Windows failed login events
- Processing security logs using AWK
- Importing external log files into Splunk
- Searching and analyzing logs using SPL
- Building visualizations for authentication monitoring
- Understanding SOC log analysis workflows

---

# Repository Structure

```text
SOC-Failed-Login-Detection/
│
├── README.md
├── Documentation/
│   └── SOC Failed Login Detection.pdf
│
└── Screenshots/
    ├── 01_Generated_Failed_Login_Events.png
    ├── 02_AWK_Log_Analysis.png
    ├── 03_CSV_Data_Import_Success.png
    ├── 04_Imported_Failed_Login_Events.png
    ├── 05_Failed_Login_Raw_Log_Analysis.png
    └── 06_Failed_Login_Event_Timeline.png
```

---

# Author

**VAISHNAVI MORE **

Cybersecurity Enthusiast | SOC Analyst | Blue Team | SIEM | Splunk
