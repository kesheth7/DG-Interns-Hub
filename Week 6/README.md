# Week 6 — Web Security Fundamentals & VAPT Portfolio

**Intern:** Swarnachandran Kesheth  
**Intern ID:** `DG/15/OCT/CYBER/132`  
**Organization:** DG Interns Hub — Cybersecurity Internship Portfolio  
**Focus Area:** Web Security Fundamentals, OWASP Top 10:2021, Automated Scanning & Manual VAPT

---

## 📋 Overview

This directory contains all deliverables completed during **Week 6** of the Cybersecurity Internship. The engagement covered end-to-end Vulnerability Assessment and Penetration Testing (VAPT) across deliberately vulnerable targets (**DVWA** at Low and Medium security levels, and **Metasploitable 2**) within an isolated Host-Only virtual network, supplemented by theoretical study notes and external hands-on labs.

---

## 📂 Repository Structure

```text
Week 6/
├── README.md                                        # Portfolio overview and deliverable index
├── Week6_Weekly_Summary_Report.pdf                  # Consolidated Week 6 VAPT & Web Security Report
├── Cheat Sheet/
│   └── VAPT_Cheat_Sheet.docx                        # Quick-reference VAPT commands, payloads & CVSS guide
├── Findings/
│   ├── 01_HostOnly_Network_Isolation.png            # Host-Only network isolation proof
│   ├── 02_Nmap_sV_Scan.png                          # Nmap service & version enumeration output
│   ├── 03_DVWA_Setup_Page.png                       # DVWA environment setup verification
│   ├── 04_DVWA_Security_Low.png                     # DVWA Low-tier configuration
│   ├── 05_ZAP_Scan_Alerts.png                       # OWASP ZAP automated active scan alerts
│   ├── DVWA_ZAP_Report.html                         # Full exported OWASP ZAP scan report
│   ├── low/                                         # DVWA Low-tier manual exploitation screenshots
│   └── medium/                                      # DVWA Medium-tier filter bypass screenshots
├── Notes/
│   ├── Q1_VA_vs_Pentest_vs_RedTeam.docx             # Assessment paradigms & 5-phase VAPT lifecycle
│   ├── Q2_Scope_RoE_and_Authorization.docx          # Governance, scope boundaries & 8-field RoE template
│   ├── Q3_OWASP_Top_10.docx                         # OWASP Top 10:2021 attack scenarios & defenses
│   ├── Q4_SQL_Injection_Types_and_Prevention.docx   # In-Band, Blind & OAST SQLi + prepared statements
│   ├── Q5_XSS_and_CSRF.docx                         # Reflected, Stored, DOM XSS vs. CSRF mitigations
│   ├── Q6_Command_Injection_LFI_RFI_FileUpload.docx # Command injection, LFI/RFI & file upload security
│   ├── Q7_Auth_Session_Flaws_and_SOC_Detection.docx # Brute-force, session hardening & SOC detection rules
│   ├── Q8_CVSS_v31_Metrics_and_Scoring.docx         # CVSS v3.1 base metrics & severity scoring breakdown
│   └── Q9_Security_Tool_Comparison.docx             # Burp Suite, ZAP, Nmap, Nikto, sqlmap & Hydra comparison
├── Payloads/
│   └── payloads.txt                                 # Curated SQLi, XSS, CMDi & LFI testing payloads
├── VAPT Report/
│   └── DVWA_Mutillidae_VAPT_Report-v2.docx          # Detailed technical VAPT findings & remediation report
└── Writeups/
    ├── TryHackMe_SQL_Injection_Writeup.docx         # TryHackMe SQL Injection room writeup (100% completed)
    ├── PortSwigger_SQLi_Lab1_Hidden_Data.docx       # PortSwigger Lab 1: WHERE clause hidden data retrieval
    └── PortSwigger_SQLi_Lab2_Login_Bypass.docx      # PortSwigger Lab 2: Administrator login bypass
```

---

## 🎯 Key Achievements & Findings Summary

* **Confirmed Exploitable Vulnerabilities (DVWA Low & Medium):**
  * **OS Command Injection (CVSS 9.8 — Critical):** Executed arbitrary OS commands (`127.0.0.1; id` and `127.0.0.1 && whoami`) achieving `www-data` execution.
  * **In-Band SQL Injection (CVSS 9.8 — Critical):** Extracted user credential hashes via `UNION SELECT` database enumeration.
  * **Unrestricted File Upload (CVSS 9.8 — Critical):** Bypassed Medium-tier MIME filtering by modifying `Content-Type: image/jpeg` to upload `shell.php` and achieve Remote Code Execution (RCE).
  * **Authentication Brute Force (CVSS 8.1 — High):** Recovered valid administrative credentials using Hydra HTTP GET dictionary attacks.
  * **Reflected & Stored XSS (CVSS 6.1 & 5.4 — Medium):** Executed arbitrary JavaScript payloads in victim browser contexts.
* **External Labs Completed:**
  * **TryHackMe:** *SQL Injection (`sqlinjectionlm`)* — 100% Completed (All 10 tasks & flags).
  * **PortSwigger Web Security Academy:** Completed *SQL injection in WHERE clause* and *SQL injection login bypass* labs.

---

## 🛠️ Primary Toolchain

* **Operating Systems & Targets:** Kali Linux, Metasploitable 2, DVWA v1.0.7 (Isolated Host-Only Virtual Network)
* **Scanning & Proxy Tools:** Nmap (`-sV`), OWASP ZAP 2.17.0, Burp Suite Community Edition
* **Exploitation & Scoring:** Hydra, FIRST CVSS v3.1 Calculator

---

> **Disclaimer:** All testing activities documented in this repository were conducted strictly within an isolated, offline Host-Only virtual lab environment and authorized educational platforms for defensive learning purposes.