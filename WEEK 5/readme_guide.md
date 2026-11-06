# DG Interns Hub — Week 5 SOC Analyst Internship Submission

[![Track](https://img.shields.org/badge/Track-SOC%20Analyst%20%2F%20Cybersecurity-blue.svg)](https://github.com/)
[![Environment](https://img.shields.org/badge/SIEM-Splunk%20Enterprise%2010.6.1-orange.svg)](https://www.splunk.com/)
[![OS](https://img.shields.org/badge/OS-Ubuntu%20Linux-E95420.svg)](https://ubuntu.com/)
[![Status](https://img.shields.org/badge/Status-Completed%20%2F%20Submitted-brightgreen.svg)](https://github.com/)

---

## 📋 Table of Contents
1. [Project Overview](#1-project-overview)
2. [Week 5 Objectives](#2-week-5-objectives)
3. [Complete Folder Structure](#3-complete-folder-structure)
4. [Folder Descriptions](#4-folder-descriptions)
5. [Tools and Technologies](#5-tools-and-technologies)
6. [Practical Work Summary](#6-practical-work-summary)
   - [6.1 SIEM Setup & Log Analysis](#61-siem-setup--log-analysis)
   - [6.2 Splunk Detection Searches](#62-splunk-detection-searches)
   - [6.3 Alert Triage Exercises](#63-alert-triage-exercises)
   - [6.4 Threat Intelligence Enrichment](#64-threat-intelligence-enrichment)
   - [6.5 Brute-Force Response Playbook](#65-brute-force-response-playbook)
   - [6.6 L1-to-L2 Escalation Ticket](#66-l1-to-l2-escalation-ticket)
   - [6.7 False-Positive Analysis](#67-false-positive-analysis)
   - [6.8 Professional Engagement & Community Sharing](#68-professional-engagement--community-sharing)
7. [Learning Outcomes](#7-learning-outcomes)
8. [Task Completion Checklist](#8-task-completion-checklist)

---

## 1. Project Overview

* **Program:** DG Interns Hub — Cybersecurity Internship
* **Module:** Week 5 Final Submission
* **Role:** Tier 1 SOC Analyst Intern
* **Intern Name:** Gunjan
* **Theme:** *Checking Alerts – The L1 Job*
* **Primary Objective:** Master practical Tier 1 Security Operations Center (SOC) workflows, including Security Information and Event Management (SIEM) log monitoring, Search Processing Language (SPL) query formulation, Open Source Intelligence (OSINT) threat enrichment, alert triage, false-positive evaluation, Standard Operating Procedure (SOP) playbook execution, and formal Tier 1 to Tier 2 (L1-to-L2) incident escalation.

---

## 2. Week 5 Objectives

The Week 5 curriculum bridges defensive security principles with practical Tier 1 SOC Analyst responsibilities:

### Theoretical Objectives
* Understand SIEM, SOAR, and EDR platform architectures and operational roles.
* Learn Splunk schema-on-read parsing (`index=main`, `sourcetype=linux_secure`) vs. Wazuh schema-on-write architecture.
* Study Linux security logging mechanisms (`/var/log/auth.log`) and Pluggable Authentication Modules (PAM).
* Differentiate between True Positives (TP), False Positives (FP), and Benign True Positives (BTP).
* Analyze Indicators of Compromise (IOC) vs. Indicators of Attack (IOA) using the MITRE ATT&CK framework.

### Practical Objectives
* Deploy and configure Splunk Enterprise `10.6.1.1` on an Ubuntu Linux virtual machine (`ubuntu-soc`).
* Execute 7 core SPL detection searches covering authentication failures, account creation, PowerShell execution, network scanning, phishing keywords, and elevated command execution.
* Perform OSINT threat intelligence enrichment using VirusTotal, AbuseIPDB, and AlienVault OTX.
* Triage 5 security alert scenarios and document investigation findings.
* Investigate a benign account creation alert (`useradd splunk`) and formulate context-aware rule tuning guidelines.
* Engineer a 6-stage Brute Force Incident Response Playbook and write an executive L1-to-L2 Incident Escalation Ticket.

---

## 3. Complete Folder Structure

```
DG Interns HUB/
└── Week 5/
    ├── Notes/
    │   ├── Q1_Alert_Triage
    │   ├── Q2_True_Positive_and_False_Positive
    │   ├── Q3_SOC_Severity_Levels
    │   ├── Q4_Escalation_Policy
    │   ├── Q5_SOC_Playbooks
    │   ├── Q6_Threat_Intelligence_Platforms
    │   ├── Q7_IOC_vs_IOA
    │   ├── Q8_MITRE_ATT&CK_Techniques
    │   ├── Q9_Splunk_Brute_Force_Detection
    │   ├── Q10_False_Positive_Handling
    │   ├── Q11_L1_to_L2_Escalation_Template
    │   └── Brute_Force_Response_Playbook
    │
    ├── Writeups/
    │   ├── Week_5_SIEM_Lab_Writeup
    │   └── Tool_Setup_and_Log_Ingestion_Notes
    │
    ├── Findings/
    │   ├── Week_5_False_Positive_Analysis
    │   ├── Lab_Findings/
    │   └── Evidence/
    │
    ├── Indicators Spreadsheet/
    │   ├── Week_5_Threat_Intelligence_Analysis.xlsx
    │   └── Indicator_Enrichment_Methodology
    │
    ├── Search Queries/
    │   ├── Week_5_Splunk_Detection_Search_Queries
    │   ├── SPL_Query_01_Brute_Force
    │   ├── SPL_Query_02_New_Account
    │   ├── SPL_Query_03_PowerShell
    │   ├── SPL_Query_04_Network_Scanning
    │   ├── SPL_Query_05_Phishing
    │   ├── SPL_Query_06_Linux_Authentication
    │   └── SPL_Query_07_Privileged_Commands
    │
    ├── Alert Reports/
    │   ├── Alert_Report_01
    │   ├── Alert_Report_02
    │   ├── Alert_Report_03
    │   ├── Alert_Report_04
    │   ├── Alert_Report_05
    │   └── L1_to_L2_Escalation_Ticket
    │
    ├── Evidence/
    │   ├── Splunk_Screenshots/
    │   ├── Alert_Triage_Screenshots/
    │   └── Threat_Intelligence_Screenshots/
    │
    ├── DG_Interns_Hub_Week_5_Final_Internship_Report.docx
    ├── DG_Interns_Hub_Week_5_Final_Internship_Report.pdf
    ├── DG_Interns_Hub_Week_5_Presentation.pptx
    └── README.md
```

---

## 4. Folder Descriptions

| Folder Name | Description & Contents |
|---|---|
| `Notes/` | Theoretical research notes answering the 11 Week 5 curriculum questions (SIEM vs. EDR, PAM logging, FP vs. TP, MITRE ATT&CK taxonomy) along with the initial draft of the Brute Force Response Playbook. |
| `Writeups/` | Technical lab write-ups detailing the installation, configuration, and data ingestion parameters for Splunk Enterprise 10.6.1 on Ubuntu Linux. |
| `Findings/` | In-depth root-cause analysis documents, including the dedicated `Week_5_False_Positive_Analysis` report for the `useradd splunk` event and core lab observation summaries. |
| `Indicators Spreadsheet/` | Threat intelligence matrix (`Week_5_Threat_Intelligence_Analysis.xlsx`) detailing IP reputation scores, file hash sandbox results, and enrichment methodology notes. |
| `Search Queries/` | Formatted SPL documentation (`Week_5_Splunk_Detection_Search_Queries`) containing exact queries, parameters, syntax breakdowns, and actual execution event counts for all 7 detection searches. |
| `Alert Reports/` | Individual incident triage reports (Alert Reports 01 through 05) detailing IOC extraction, decision logs, and the formal `L1_to_L2_Escalation_Ticket`. |
| `Evidence/` | Image artifacts, raw log extracts, and verified screenshots proving VirtualBox setup, Splunk query executions, OSINT platform lookups, and cloud folder structures. |
| **Root Files** | Master executive deliverables including `DG_Interns_Hub_Week_5_Final_Internship_Report` (.docx & .pdf), the final slide deck (`DG_Interns_Hub_Week_5_Presentation.pptx`), and this repository guide (`README.md`). |

---

## 5. Tools and Technologies

The following software platforms, utilities, and frameworks were used during Week 5:

* **Splunk Enterprise 10.6.1.1:** SIEM platform used for indexing `/var/log/auth.log`, writing SPL queries, analyzing event statistics, and building detection rules.
* **Ubuntu Linux (Host: `ubuntu-soc`):** Target operating system hosted on Oracle VirtualBox, generating Linux security and PAM authentication telemetry.
* **VirusTotal:** OSINT platform used to analyze file hashes (MD5/SHA256) and domain reputations across 70+ antivirus engines.
* **AbuseIPDB:** Threat intelligence database used to check IP address abuse confidence scores and geolocation metadata.
* **AlienVault OTX:** Open Threat Exchange platform used to correlate IOCs against community threat pulses and malicious infrastructure.
* **MITRE ATT&CK Framework:** Enterprise matrix used to map endpoint telemetry and alerts to standardized adversary tactics and techniques.
* **Microsoft Excel / Office Suite:** Used to compile structured threat intelligence matrices, technical write-ups, and executive reports.

---

## 6. Practical Work Summary

### 6.1 SIEM Setup & Log Analysis
Splunk Enterprise 10.6.1.1 was configured on the `ubuntu-soc` virtual machine. System authentication logs from `/var/log/auth.log` were ingested into Splunk under `index=main` and `sourcetype=linux_secure`.

### 6.2 Splunk Detection Searches
Formulated and executed 7 core Search Processing Language (SPL) detection queries:
1. **Brute Force Detection:** `index=main sourcetype=linux_secure ("authentication failure" OR "Failed password") | stats count as failed_attempts by host, process, logname | sort - failed_attempts` *(Result: 4 events / 2 summary rows for user `gunjan`)*
2. **New Account Creation Detection:** `index=main sourcetype=linux_secure ("useradd" OR "adduser") | table _time host _raw | sort -_time` *(Result: 1 event for user `splunk`, UID 1001, GID 1001)*
3. **Suspicious PowerShell Activity:** `index=main sourcetype=linux_secure ("useradd" OR "adduser") | search Image="*powershell.exe*" | table _time host user Image CommandLine | sort -_time` *(Result: 0 events — Windows Sysmon telemetry boundary)*
4. **Network Service Scanning Detection:** `index=* ("SYN Scan" OR "port scan" OR "Nmap") | table _time host source src_ip dest_ip _raw | sort -_time` *(Result: 0 events — Firewall/NIDS telemetry boundary)*
5. **Phishing Activity Detection:** `index=* ("phishing" OR "phish" OR "suspicious attachment") | table _time host source _raw | sort -_time` *(Result: 0 events — Mail gateway telemetry boundary)*
6. **Linux Authentication Failure Analysis:** `index=main sourcetype=linux_secure ("authentication failure" OR "Failed password") | stats count as failure_count values(process) as processes by host, logname | sort - failure_count` *(Result: 4 events / 1 summary row for user `gunjan`)*
7. **Privileged Command Monitoring:** `index=main sourcetype=linux_secure "COMMAND=" | table _time host _raw | sort -_time` *(Result: 33 events capturing `sudo` and `pkexec` invocations)*

### 6.3 Alert Triage Exercises
Evaluated 5 standardized alert scenarios, extracting log attributes, checking OSINT indicators, classifying risk, and defining response steps:
* **Alert 01 (SSH Brute Force):** True Positive — External brute-force pattern targeting SSH daemon.
* **Alert 02 (New Account Creation):** Benign True Positive — Service account setup for Splunk.
* **Alert 03 (Privilege Elevation):** Benign True Positive — Authorized administrative `sudo` commands.
* **Alert 04 (Suspicious Script Execution):** True Positive — Unauthorized execution of shell script in `/tmp`.
* **Alert 05 (Unauthorized Port Scan):** True Positive — Internal host generating outbound port scanning traffic.

### 6.4 Threat Intelligence Enrichment
Audited network indicators and file hashes using VirusTotal, AbuseIPDB, and AlienVault OTX. Formatted findings into `Week_5_Threat_Intelligence_Analysis.xlsx`, identifying clean internal assets versus malicious scanners and command-and-control (C2) nodes.

### 6.5 Brute-Force Response Playbook
Engineered a 6-phase Incident Response Playbook following NIST standards:
$$\text{Preparation} \longrightarrow \text{Identification} \longrightarrow \text{Containment} \longrightarrow \text{Eradication} \longrightarrow \text{Recovery} \longrightarrow \text{Lessons Learned}$$

### 6.6 L1-to-L2 Escalation Ticket
Drafted a formal L1-to-L2 Incident Escalation Ticket (`ESCALATION-SOC-2026-1106`) transferring a high-priority incident (SSH brute force followed by successful logon) to Tier 2 handlers with attached SIEM logs and perimeter containment recommendations.

### 6.7 False-Positive Analysis
Performed a root-cause investigation on the `useradd` event for user `splunk` (UID 1001, GID 1001). Documented why the event aligned with software deployment and provided context-aware detection tuning guidelines to avoid blanket suppression.

### 6.8 Professional Engagement & Community Sharing
Documented learning milestones, key technical takeaways, and project deliverables to share with the cybersecurity community on LinkedIn.

---

## 7. Learning Outcomes

By completing Week 5 practical tasks, key Tier 1 SOC competencies were developed:
* **SIEM Query Engineering:** Formulating, refining, and optimizing Search Processing Language (SPL) queries in Splunk Enterprise.
* **Log Telemetry Parsing:** Extracting core event attributes (`_raw`, `PID`, `tty`, `logname`, `host`) from Linux `/var/log/auth.log`.
* **OSINT Enrichment:** Conducting external threat lookups across VirusTotal, AbuseIPDB, and AlienVault OTX to contextualize IOCs.
* **Signal-to-Noise Tuning:** Distinguishing benign system modifications from malicious intrusion attempts to reduce alert fatigue.
* **Incident Escalation & Playbook Execution:** Writing executive escalation handoff tickets and building operational response SOPs.
* **Data Boundary Reporting:** Accurately documenting zero-result searches caused by missing log feeds (e.g., Sysmon, Firewall logs) rather than making false assumptions.

---

## 8. Task Completion Checklist

- [x] **SIEM Environment Setup:** Splunk Enterprise 10.6.1.1 configured on Ubuntu VM (`ubuntu-soc`).
- [x] **Log Ingestion:** `/var/log/auth.log` ingested under `index=main` and `sourcetype=linux_secure`.
- [x] **Splunk Detection Searches:** All 7 SPL queries executed, verified, and documented with exact event counts.
- [x] **Theoretical Q&A Notes:** Completed answers for all 11 Week 5 theoretical questions.
- [x] **Alert Triage Reports:** Triaged and compiled Alert Reports 01 through 05.
- [x] **Threat Intelligence Matrix:** Audited indicators and populated `Week_5_Threat_Intelligence_Analysis.xlsx`.
- [x] **False Positive Report:** Authored `Week_5_False_Positive_Analysis` detailing `useradd splunk` context and rule tuning recommendations.
- [x] **Incident Response Playbook:** Engineered 6-phase Brute Force Response Playbook.
- [x] **L1-to-L2 Handoff Ticket:** Compiled formal L1-to-L2 Escalation Ticket (`ESCALATION-SOC-2026-1106`).
- [x] **Final Deliverables:** Compiled Master Final Internship Report (`.docx` & `.pdf`), slide deck (`.pptx`), and GitHub guide (`README.md`).