# Week 4 – SIEM & Security Monitoring

**Internship:** DG Interns Hub – Cybersecurity Track  
**Student Name:** Gunjan  
**Submission Date:** 31 October 2026  

---

## 1. About the Project

This repository contains my complete documentation and study materials for **Week 4** of my cybersecurity internship at **DG Interns Hub**. 

During this week, I focused on learning how Security Operations Center (SOC) analysts monitor enterprise networks, analyze security logs, write detection rules, and investigate potential security incidents using tools like **Splunk**, **Wazuh**, and **Snort IDS**.

---

## 2. Week 4 Objectives

The main objectives for this week were:
* Understand what a SIEM is and how it collects and analyzes security logs.
* Learn Splunk basics and write simple Search Processing Language (SPL) queries.
* Understand the architecture and features of the open-source Wazuh platform.
* Analyze Windows Security Event Logs, focusing on login activities.
* Distinguish between successful logons (Event ID 4624) and failed logons (Event ID 4625).
* Understand how event correlation and threshold-based alerts work.
* Learn how to write and configure custom Snort Local Rules.
* Map network port scanning and brute-force attacks to the MITRE ATT&CK framework.

---

## 3. Topics Covered

Here is a quick summary of the main topics studied during Week 4:

* **SIEM vs SOAR vs EDR:** Understanding how SIEM (log correlation), SOAR (automated response), and EDR (endpoint monitoring) work together in a SOC.
* **Splunk vs Wazuh:** Comparing Splunk (commercial big-data search engine) with Wazuh (open-source XDR/SIEM platform).
* **Splunk Architecture:** Learning the roles of Universal Forwarders (log collectors), Indexers (log storage), and Search Heads (query interface).
* **Wazuh Architecture:** Understanding how Wazuh Agents send encrypted endpoint telemetry to the central Wazuh Manager and Indexer.
* **Event Correlation:** Linking separate events across different systems to identify multi-stage attack patterns.
* **Threshold-Based Alerts:** Setting up alerts that fire when event counts cross a specific limit (e.g., more than 10 failed logins in 15 minutes).
* **MITRE ATT&CK T1110 (Brute Force):** Analyzing password guessing and password spraying techniques.
* **MITRE ATT&CK T1046 (Network Service Discovery):** Detecting network port scanning tools like Nmap.
* **Snort IDS & Local Rules:** Understanding rule headers, actions, protocols, and custom options in `local.rules`.

---

## 4. Tools and Technologies

* **Splunk Enterprise:** Big-data log analytics and SPL search queries.
* **Wazuh:** Open-source host monitoring and security rules engine.
* **Snort IDS:** Network intrusion detection engine and custom packet inspection.
* **Windows 10:** Host operating system for running lab applications.
* **Kali Linux (2026.2):** Linux environment for security tools and administration.
* **Oracle VirtualBox:** Virtualization platform used for running lab VMs.
* **SPL (Search Processing Language):** Query language used in Splunk.
* **TryHackMe:** Practical learning platforms and rooms.
* **MITRE ATT&CK Framework:** Knowledge base for tracking adversary tactics and techniques.

---

## 5. Previous Practical Work

Prior to this week, I built practical experience using Splunk Enterprise in a local home lab environment:
* **Log Ingestion:** Ingested and analyzed local Windows Security Event Logs (`WinEventLog:Security`).
* **Event ID 4624 Analysis:** Audited successful logons and examined different connection types (e.g., Logon Type 2 for console, Type 10 for RDP).
* **Event ID 4625 Analysis:** Investigated failed logon attempts to identify targeted accounts and source IP addresses.
* **SPL Queries:** Practised core SPL commands including `search`, `stats`, `eval`, `table`, `fields`, `dedup`, `sort`, and `timechart`.
* **Authentication Monitoring:** Built search queries to detect suspicious login spikes and potential brute-force attempts.

---

## 6. Snort Local Rules

I studied and documented five essential custom Snort local rules:
1. **ICMP Ping Detection:** Flags incoming ICMP Echo Requests (`itype:8`) to spot network discovery sweeps.
2. **SSH Connection Detection:** Monitors TCP SYN packets targeting port 22 to audit external remote login attempts.
3. **HTTP Traffic Detection:** Inspects outbound cleartext HTTP GET requests on port 80.
4. **Nmap SYN Scan Detection:** Flags TCP SYN packets matching Nmap's default window size (`window:1024`) to detect stealth scans (**MITRE T1046**).
5. **Suspicious Network Activity Detection:** Scans web traffic payloads for cleartext `password=` parameters to identify insecure login forms.

---

## 7. TryHackMe Rooms

The following TryHackMe rooms provided fundamental learning content for Week 4:
* [Introduction to SIEM](https://tryhackme.com/room/introtosiem) – Log ingestion, correlation, and alert triage fundamentals.
* [Splunk: Exploring SPL](https://tryhackme.com/room/splunkexploringspl) – SPL query syntax, command pipelines, and data transformation.
* [Wazuh](https://tryhackme.com/room/wazuhct) – Wazuh agent-manager architecture, rules engineering, and File Integrity Monitoring.

---

## 8. Project Folder Structure

```
DG Interns HUB/
└── Week 4/
    ├── Notes/               # Contains modular theoretical PDF study notes.
    ├── Writeups/            # Holds detailed TryHackMe writeups and Snort rule guides.
    ├── Search Queries/      # Stores Markdown libraries of SPL reference queries.
    ├── Snort Rules/         # Holds the custom local.rules file with Snort signatures.
    ├── Dashboard Screenshots/# Reserved folder for local lab interface captures.
    ├── Findings/            # Contains investigation notes and log triage findings.
    ├── Reports/             # Stores consolidated master internship reports (PDF/MD).
    ├── Presentation/        # Holds the Week 4 presentation slide deck (.pptx).
    └── README.md            # Repository overview and landing documentation.
```

---

## 9. Learning Outcomes

Working through Week 4 helped me build a strong foundation in security monitoring and SOC operations. I gained practical knowledge of how SIEM platforms aggregate logs, how to write SPL queries to hunt for threats in Windows authentication logs, and how to write custom Snort signatures to detect network scanning. Understanding these concepts and tool architectures makes me feel much more confident as I prepare for an entry-level SOC Analyst role.

---

## 10. Conclusion

Week 4 was a great learning experience focused on SIEM, log analytics, and threat detection. By studying Splunk, Wazuh, Windows Event logs, Snort, and the MITRE ATT&CK framework, I gained valuable knowledge about how security analysts defend enterprise networks against modern threats.