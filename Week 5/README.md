# Week 5 - SOC Analyst & Incident Response Portfolio

- **Intern:** Swarnachandran Kesheth
- **Intern ID:** DG/15/OCT/CYBER/132
- **Program:** DG Interns Hub
- **Date:** 22 November 2026

## Folder Structure

```text
Week 5/
├── Week5_Presentation_Report.pptx
├── Week5_Weekly_Report.pdf
├── README.md
├── Cheat Sheet/
│   ├── IOC_Type_Reference_Table.docx
│   └── Phishing_Red_Flag_Checklist.docx
├── Findings/
│   ├── ATTACK_Navigator/
│   │   ├── ATTACK_Navigator_Map.png
│   │   ├── ATTACK_Navigator_Report.docx
│   │   └── Week5_ATTACK_Layer.json
│   ├── Atomic_Red_Team/
│   │   ├── 01_ART_Install.png
│   │   ├── 02a_ART_T1053_Execution.png
│   │   ├── 02b_ART_T1059_T1136_Execution.png
│   │   ├── 03_Sysmon_EventID1_ART.png
│   │   ├── 04_Security_EventID4720_ART.png
│   │   ├── 05_ART_Cleanup.png
│   │   └── Atomic_Red_Team_Report.docx
│   ├── Malware_Triage/
│   │   ├── 01_Kali_EICAR_Static.png
│   │   ├── 02_Windows_Defender_EICAR.png
│   │   ├── 03_Defender_EventLog_1116.png
│   │   ├── 04_Sysmon_EventLog_EICAR.png
│   │   ├── 05_AnyRun_Report1.png
│   │   ├── 06_HybridAnalysis_Report2.png
│   │   └── Safe_Malware_Triage_Report.docx
│   └── Phishing_Analysis/
│       ├── Sample_01/ (01_Sample1_Bradesco_Livelo_Phishing_Analysis.docx + 5 screenshots)
│       ├── Sample_02/ (02_Sample2_OKX_Fake_Extension_Phishing_Analysis.docx + 7 screenshots)
│       └── Sample_03/ (03_Sample3_Casino_Promo_Phishing_Analysis.docx + 7 screenshots)
├── Incident Report/
│   └── Week5_Incident_Report.docx
├── Notes/
│   ├── 01_NIST_Incident_Response_Lifecycle.docx
│   ├── 02_Phishing_Types_and_Red_Flags.docx
│   ├── 03_SPF_DKIM_and_DMARC.docx
│   ├── 04_Email_Header_Analysis.docx
│   ├── 05_IOC_IOA_and_Pyramid_of_Pain.docx
│   ├── 06_MITRE_ATTACK_vs_Cyber_Kill_Chain.docx
│   ├── 07_Static_Dynamic_Malware_Analysis_and_Sandbox_Safety.docx
│   └── 08_Incident_Report_Fields_Severity_and_Escalation.docx
└── Writeups/
    ├── 01_TryHackMe_Cyber_Kill_Chain_Writeup.docx (+ screenshot)
    ├── 02_TryHackMe_MITRE_Premium_Limitation_Writeup.docx (+ screenshot)
    ├── 03_TryHackMe_Pyramid_of_Pain_Writeup.docx (+ screenshot)
    ├── 04_TryHackMe_Phishing_Analysis_Fundamentals_Writeup.docx (+ screenshot)
    └── 05_TryHackMe_Intro_to_Cyber_Threat_Intel_Writeup.docx (+ screenshot)
```

## Summary of Work Completed

1. **Phishing Email Investigations:** Triaged three public phishing samples (`sample-1.eml`, `sample-10.eml`, and `sample-12.eml`) using passive SMTP header checks, offline Base64/quoted-printable decoding in CyberChef, and OSINT lookups in VirusTotal, AlienVault OTX, and urlscan.io.
2. **Incident Response Report (`INC-2026-0708-002`):** Documented the deceptive OKX Web3 Chrome extension phishing email (`sample-10.eml`), including timeline, defanged IOCs, MITRE ATT&CK mapping, severity rationale, and containment recommendations.
3. **Safe Malware Triage:** Verified static hashes, strings, and metadata for the 68-byte EICAR test file on Kali Linux, confirmed Windows Defender Event ID 1116 and Sysmon Event ID 11 logs on Windows 11, and reviewed public sandbox reports on Any.Run and Hybrid Analysis.
4. **MITRE ATT&CK Navigator Coverage:** Built and exported `Week5_ATTACK_Layer.json` mapping six techniques observed across Weeks 2–5 (`T1046`, `T1110`, `T1566.002`, `T1059.001`, `T1136.001`, `T1053.005`) to SIEM and EDR detection rules.
5. **Atomic Red Team Simulation:** Executed non-destructive endpoint tests for `T1053.005`, `T1059.001`, and `T1136.001` on `DESKTOP-IBM79KA`, confirmed Sysmon and Windows Security Event Log entries, and restored baseline system state with `-Cleanup`.
6. **Cheat Sheets, Study Notes & TryHackMe Writeups:** Created a 12-category IOC reference table, a one-page phishing red-flag checklist, eight topic study notes, and five TryHackMe room writeups.
