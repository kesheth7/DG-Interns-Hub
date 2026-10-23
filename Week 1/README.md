# DG Interns Hub — Week 1

**Prepared by:** Swarnachandran Kesheth

# DG Interns Hub — Week 1 Cybersecurity Internship

## Overview

This folder documents my Week 1 learning activities and practical exercises in cybersecurity fundamentals, Linux administration, virtual machines, and basic networking. It contains individual theory notes, learning-platform writeups, practical evidence, a Linux command cheat sheet, and weekly reports.

## Week 1 Objectives

* Understand cybersecurity foundations and professional roles.
* Review networking concepts, protocols, and common ports.
* Set up and connect virtual machines in an isolated lab.
* Practice essential Linux commands and administration.
* Complete beginner learning activities on TryHackMe and OverTheWire Bandit.
* Record findings and communicate learning outcomes.

## Folder Structure

```text
DG Interns Hub/
└── Week 1/
    ├── Notes/                         # Eight separate theory Q\&A documents
    ├── Writeups/                      # Separate TryHackMe and Bandit writeups
    ├── Findings/
    │   ├── Lab Setup/                 # VM inventory, IP addresses, ping tests, snapshots
    │   ├── Linux Practice/            # Commands, users, groups, permissions, cron
    │   ├── Network Map or Diagram/    # Lab topology
    │   └── Over the Wire Bandit/      # Level evidence screenshots
    ├── Cheat Sheet/                   # 30 Linux commands table
    ├── DG\_Interns\_Hub\_Week1\_Weekly\_Report.pdf
    ├── DG\_Interns\_Hub\_Week1\_Weekly\_Report.docx
    ├── DG\_Interns\_Hub\_Week1\_Presentation\_Report.pptx
    └── README.md
```

*Folder names and report filenames may differ slightly on the local computer.*

## Theory Notes

Eight separate notes cover:

1. Cybersecurity and the CIA triad.
2. SOC analyst, penetration tester, and incident responder roles.
3. OSI and TCP/IP models, protocols, and attacks.
4. IP, MAC, DNS, DHCP, and 12 common network ports.
5. Linux filesystem hierarchy, chmod, chown, and SUID.
6. Threats, vulnerabilities, risks, and exploits.
7. NAT, NAT Network, Host-only, and Bridged VM networking.
8. Legal and ethical cybersecurity, including Sri Lankan law.

## Practical Lab Setup

The lab uses Oracle VirtualBox with Kali Linux, Ubuntu, and Windows 11 VMs. Recorded host-only IP addresses:

|Virtual machine|Host-only IP address|
|-|-|
|Ubuntu|`192.168.56.101`|
|Kali Linux|`192.168.56.102`|
|Windows 11|`192.168.56.103`|

The host-only network is `192.168.56.0/24`. NAT adapters were used for internet connectivity where configured. Captured ICMP ping tests show successful communication between the tested VMs. A Kali snapshot was also recorded. Metasploitable2 was part of the planned lab, but its network configuration and testing should be verified separately before claiming completion.

**Safety:** Deliberately vulnerable systems must remain isolated from public or production networks. Do not bridge a vulnerable VM to an untrusted network.

## Linux Practice

Exercises included file and directory operations, users and groups, ownership and permissions, and cron-related practice. The `Cheat Sheet` folder contains **exactly 30 Linux commands** with columns for command, what it does, and when to use it.

> Verification note: Some administrative configurations, including final shared-directory permissions and cron execution, may require a final check against screenshots or command output.

## Learning Platform Writeups

* **TryHackMe:** Eight individual room writeup files were prepared. The documented topics include Search Skills, Learning Cyber Security, Linux Fundamentals Part 1, Introductory Networking, Networking Concepts, Intro to LAN, Pyramid of Pain, and What Is Networking. Verify each room's completion evidence before final submission.
* **OverTheWire Bandit:** Individual writeup files were prepared for levels 0–11. The screenshots demonstrate selected logged-in levels; not every command or level transition is visible in the evidence. Check writeups against the steps actually performed.

Writeups summarize the learning objective, activities, outcomes, and available screenshots. Credentials and passwords should not be published.

## Reports

* **Weekly PDF report:** Summary of lab setup, networking tests, Linux activities, learning platforms, and outcomes.
* **Editable Word report:** Working copy of the weekly report.
* **Presentation report:** Slides summarizing the week's activities and evidence.

## Main Learning Outcomes

* Created a basic isolated multi-VM cybersecurity lab.
* Assigned and tested host-only VM networking addresses.
* Used ICMP ping to verify network connectivity.
* Practiced foundational Linux administration concepts.
* Reviewed cybersecurity, networking, and threat-analysis concepts through structured notes and training rooms.
* Organized screenshots and produced professional documentation.

## Submission Checklist

* \[x] Notes — eight separate files
* \[x] Writeups — separate draft files for TryHackMe rooms and Bandit levels
* \[x] Findings — screenshots organized into task folders
* \[x] Cheat Sheet — exactly 30 Linux commands
* \[x] Weekly PDF report
* \[x] Presentation report
* \[x] README file
* \[x] Final review: confirm screenshot-to-writeup accuracy, any unverified lab tasks, and all required files
* \[x] Upload/share the complete Week 1 folder using the submission method specified by the internship coordinator

## Ethical Use

All practical work should be performed only in authorized environments, within the agreed scope. Keep credentials, personal information, and sensitive data out of shared documentation.

