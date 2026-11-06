# DG Interns Hub — Week 3

**Topic:** Linux Logs, Sysmon, auditd and Snort Setup  
**Learner:** Kesheth Swarnachandran  
**Week 3 deadline listed in guide:** 2026-11-06, 11:59 PM  
**Evidence basis:** supplied Week 3 ZIP, original rules and captured screenshots.

## Status overview

| Area | Status |
|---|---|
| 10 theory questions | 10 separate DOCX notes included |
| TryHackMe (4 rooms) | Learner reports completed; four progress-page screenshots |
| LetsDefend (6 courses) | Five learner-reported complete; Incident Response on Linux partial due VIP+ lab |
| Windows Sysmon | IDs 1, 3 and 11 captured and explained |
| Ubuntu auditd | apt install nano found via ausearch -k nano -i |
| Snort | Four tested alerts/rules, including SID 1000004 mapped to ATT&CK T1046 |
| Cheat sheet | 16 events and rules |
| LinkedIn | Two posts required by guide; publication is an external pending action |
| Google Drive / submission | User action needed |

## Topology

- Ubuntu 192.168.56.101: Snort 2.9.20 on enp0s8 and auditd.
- Kali 192.168.56.102: permitted internal test traffic.
- Windows 11 192.168.56.104: Sysmon capture.
- VirtualBox host-only subnet: 192.168.56.0/24.

## Key verification commands

```bash
sudo auditctl -w /usr/bin/apt -p x -k nano
sudo apt install nano
sudo ausearch -k nano -i
sudo snort -T -i enp0s8 -c /etc/snort/snort.conf
sudo snort -A console -q -c /etc/snort/snort.conf -i enp0s8
sudo nmap -sS -T4 -p 1-1000 192.168.56.101
```

Windows: `sysmon.exe -accepteula -i sysmonconfig-export.xml`. View `Microsoft-Windows-Sysmon/Operational` in Event Viewer.

## Rule-scope note

`HOME_NET=192.168.56.0/24`; `EXTERNAL_NET=any` was intentionally used **only for this isolated lab** because Kali is within HOME_NET. The guide's default `!$HOME_NET` would exclude source Kali from SID 1000004. A real deployment must use carefully scoped variables, thresholds and false-positive review.

## Limitation: LetsDefend VIP+

The Incident Response on Linux course was readable, but the lab `Connect` action opened a VIP+ page listing $39.99/month. Practical evidence could not be queried, so account name, webshell name, reverse-shell IP and SSH-key questions remain unverified. `Findings/LetsDefend/premium.png` is the screenshot. The lesson was **partially** completed, not fully completed.

## Troubleshooting documented

1. Windows user creation permissions: System error 5 -> ran elevated PowerShell.
2. VirtualBox Ubuntu guest integration and package typo: used `virtualbox-guest-x11` and shared folder `Week3Share`.
3. Snort interface mismatch: verified `enp0s8` with `ip a`.
4. Snort EXTERNAL_NET scope: adapted for same-subnet testing and documented trade-offs.
5. LetsDefend lab VIP+ restriction: saved screenshot and did not invent answers.

## Directory guide

- `Notes/`: 10 independent theory DOCX files.
- `Writeups/TryHackMe/`: 4 room writeups, individual.
- `Writeups/LetsDefend/`: 6 course writeups, including partial course.
- `Writeups/Hands-On/`: Sysmon, auditd, starter Snort, T1046 tests.
- `Findings/`: original images grouped by platform.
- `Snort Rules/`: the original `Week3_local.rules` uploaded by learner.
- `Cheat Sheet/`: DOCX and CSV (16 entries).
- `PDF Report/`: PDF and editable Word weekly reports. `Presentation Report/`: PowerPoint weekly presentation.
- The four extra root files (evidence inventory, submission checklist, and two LinkedIn draft TXT files) were intentionally excluded to match the Week 1/2 folder style. LinkedIn posting and final submission are still required externally.

## Evidence integrity

Screenshots and rule file were copied from the uploaded ZIP without content alteration. Course screenshots often show progress/course pages; do not treat them as task-by-task command transcripts. The screenshot filenames and folder locations identify the evidence. All network testing was restricted to this authorized VirtualBox lab.
