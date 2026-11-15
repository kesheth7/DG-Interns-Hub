# DG Interns Hub - Week 4

**Topic:** SIEM in Practice: Splunk, Wazuh and Log Ingestion  
**Prepared by:** Swarnachandran Kesheth  
**Intern ID:** DG/15/OCT/CYBER/132  
**Deadline:** 15 November 2026, 11:59 PM IST

## Summary

This week I created a Splunk `lab` index, ingested Windows Security, Sysmon and Ubuntu authentication logs, ran five SPL detections, configured two scheduled alerts, built a four-panel SOC dashboard, and investigated controlled SSH brute-force and Nmap SYN scan activity. I deployed a separate Wazuh server, enrolled an Ubuntu and Windows endpoint, observed file integrity alerts and tested a custom rule with `wazuh-logtest`.

## Folder guide

|Folder|Contents|
|-|-|
|`Notes/`|Eight theory answers in separate Word files|
|`Writeups/`|Two TryHackMe writeups, with completion screenshots|
|`Findings/Splunk\_Setup/`|Splunk login, index and receiving port evidence|
|`Findings/Log\_Ingestion/`|Ubuntu/Windows forwarders and event search evidence|
|`Findings/Attack\_to\_Alert/`|Separate SSH and Nmap writeups and raw/parsed/detection screenshots|
|`Findings/Triage\_Notes/`|Three L1 triage notes|
|`Findings/Dashboard/`|Four-panel dashboard screenshots|
|`Detections/SPL\_Searches/`|Five documented SPL detections and result evidence|
|`Detections/Scheduled\_Alerts/`|Scheduled alert configuration and trigger evidence|
|`Detections/Wazuh/`|Custom rule, rule test note and Wazuh dashboard, agent, FIM screenshots|
|`Cheat Sheet/`|SPL and SIEM alert lookup tables|
|`PDF Report/`|Weekly report with selected screenshots|
|`PPT Report/`|Editable presentation with selected screenshots|

## Evidence-based accomplishments

1. Splunk `lab` index created and receiving logs from Windows and Ubuntu.
2. SSH brute-force simulation: Kali `192.168.56.102` to Ubuntu `192.168.56.101`, 20-word Hydra list; unsuccessful guesses detected in Splunk and scheduled alert triggered. MITRE ATT\&CK T1110.
3. Nmap SYN scan from Kali to Ubuntu detected by Snort T1046 rule and surfaced in Splunk.
4. Five SPL searches: EventCode 4625, Sysmon Event ID 1 PowerShell, EventCode 4720, Ubuntu SSH failures, and rare process parents/children.
5. Scheduled SSH brute-force and Windows new-account alerts configured; dashboard comprises four panels.
6. Wazuh Ubuntu and Windows agents both active in screenshot 59.
7. Wazuh FIM added and modified `/home/ubuntu/wazuh\_fim\_test/test.txt`, rule IDs 554 and 550.
8. Custom rule ID 100100, level 8, verified through `wazuh-logtest`.
9. Two TryHackMe rooms completed to 100 percent.

## Issues and fixes learned

**Wazuh download issue:** The initial `http://packages.wazuh.com/4.41/wazuh-install.sh` saved XML instead of a Bash script. Executing it produced `syntax error near unexpected token newline` and `<?xml version=...`. I downloaded from the HTTPS versioned endpoint `https://packages.wazuh.com/4.14/wazuh-install.sh`, confirmed the `#!/bin/bash` header and successfully installed Wazuh 4.14.10.

**Duplicate installation attempt:** Re-running the installer yielded `Wazuh manager already installed`, `Wazuh indexer already installed`, and `Wazuh dashboard already installed`. The earlier installation had succeeded, so I avoided the `--overwrite` option, which would erase configuration and data.

**Network reachability issue:** The Wazuh host-only address `192.168.56.105` was initially unreachable from Windows. Host-only routing/adapter and Ubuntu `enp0s8` configuration were inspected. Later the dashboard opened at `https://192.168.56.105` and agent enrollment succeeded.

**Windows MSI download issue:** `Invoke-WebRequest` encountered a forcibly closed remote connection. Retrying downloaded the MSI; I verified the resulting file and installed the Windows Wazuh agent, which reported active.

## Validation and transparency

The attack traffic was authorized and generated inside my private VirtualBox lab. A SIEM alert confirms suspicious behavior matching the detection rule, not unauthorized compromise. The submitted Wazuh XML is a reproducible version of the tested matching rule; compare with the VM's original configuration if an exact deployed-file copy is required.

**LinkedIn:** Two posts are required (SIEM concept and weekly dashboard/detection). Publishing them cannot be verified from the uploaded screenshots; complete and link them before submission.

## Submission checklist

* \[x] Eight theory notes
* \[x] Two THM writeups
* \[x] Splunk index and log ingestion evidence
* \[x] Wazuh dashboard, agents and FIM evidence
* \[x] SSH and Nmap attack-to-alert writeups
* \[x] Five SPL detection documents
* \[x] Two scheduled alerts, four-panel dashboard evidence
* \[x] Wazuh custom rule test evidence
* \[x] Three triage notes and two cheat sheets
* \[x] PDF weekly report and PowerPoint presentation
* \[x] Verify LinkedIn concept and weekly posts are published
* \[x] Upload folder to Drive and submit the folder link before the deadline

