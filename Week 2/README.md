# DG Interns Hub — Week 2

**Topic:** Network Traffic Analysis, Nmap and Windows Logging  
**Submission deadline:** 30 October 2026, 11:59 PM IST

## Work completed and included
- **Notes:** 8 separate theory DOCX files.
- **Writeups:** 6 TryHackMe room DOCX writeups, 6 completion screenshots, and a Wireshark practical DOCX writeup.
- **Wireshark:** TCP handshake, HTTP GET, DNS query and ICMP echo screenshots; 2 protocol-traffic PCAPNG files.
- **Nmap:** Ubuntu and Windows -sn, -sS, -sV, -O, -A; 20 TXT/XML outputs, scan screenshots, and a SYN/RST PCAPNG.
- **Windows events:** screenshots for 4625, 4624 (including observed logon type 5), 4720, 4732, 7045 and 1102; Security log EVTX backup.
- **PowerShell:** Get-WinEvent / FilterHashtable evidence, failed-logon CSV, Group-Object screenshot; 3 failed logons for `kesheth` in controlled lab.
- **Cheat Sheets:** 20 Wireshark filters and 15 Windows Security Event IDs.
- **PDF Report:** weekly report provided in **DOCX and PDF**.
- **Presentation Report:** editable PPTX slide deck.

## Key observed scan results
- Ubuntu 192.168.56.101: TCP/80 open, 999 other scanned TCP ports closed in SYN scan.
- Windows 192.168.56.104: all 1,000 scanned TCP ports filtered (no response) in SYN scan.

## Evidence organisation
- `Notes/`: theory answers.
- `Writeups/`: six TryHackMe writeups and Wireshark practical writeup.
- `Findings/`: screenshots of practical evidence.
- `Captures/`: PCAPNG and Nmap TXT/XML output.
- `Cheat Sheets/`: two reference documents.
- `PDF Report/`: Word and PDF weekly report.
- `Presentation Report/`: PowerPoint presentation.
- `Documentation/`: original README and updated submission checklist.

## Final manual checks before submission
- Confirm LinkedIn concept post and weekly post are actually published, tagging DG Interns Hub.
- Upload the complete `Week 2` folder to the internship Google Drive and submit its accessible shared link.
- Check that screenshots and documents are readable and that the Drive link permissions allow reviewer access.
- Wireshark sample-capture analysis is listed as **fallback/extra**, not a mandatory replacement for the completed six TryHackMe rooms.

## Scope and integrity
All practical findings relate to controlled virtual machines. Screenshots and saved logs provide evidence; this README does not claim a confirmed attack or independently verify LinkedIn publication or Google Drive submission.
