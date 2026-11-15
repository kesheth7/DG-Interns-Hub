# Wazuh custom rule test

- Test location: Wazuh manager VM (`wazuh-server`).
- Example log: `Nov 15 10:00:00 ubuntu week4lab: UNAUTHORIZED_CHANGE detected in security configuration`.
- Test command: `sudo /var/ossec/bin/wazuh-logtest`.
- Observed result: rule ID **100100**, level **8**, description **Week 4: Suspicious configuration change detected**, `Alert to be generated`.
- Evidence: `Evidence/61_Wazuh_Custom_Rule_Logtest.png`.

The included `local_rules.xml` reproduces the demonstrated matching condition for submission. Compare it against the actual `/var/ossec/etc/rules/local_rules.xml` on the VM if submitting the verbatim deployed configuration is required.
