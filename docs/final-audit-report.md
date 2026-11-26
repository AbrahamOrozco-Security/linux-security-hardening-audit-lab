# Final Security Audit Report

## 1. Overview

This project involved a manual security audit and hardening of an Ubuntu Server 24.04.5 LTS virtual machine.

Twelve security controls were reviewed using Linux command-line tools. Lynis 3.1.7 was subsequently used to perform an independent automated assessment and compare its results with the manual audit.

## 2. Manual Audit Results

All 12 controls were completed and documented.

| ID | Security Control | Status |
|---|---|---|
| C01 | System Inventory | Completed |
| C02 | Users and Groups | Completed |
| C03 | Privileged Accounts | Completed |
| C04 | Sudo Privileges | Completed |
| C05 | Critical File Permissions | Completed |
| C06 | SSH Service | Completed |
| C07 | SSH Root Login | Completed |
| C08 | SSH Authentication Method | Completed |
| C09 | Firewall | Completed |
| C10 | Listening Ports and Services | Completed |
| C11 | Security Updates | Completed |
| C12 | Authentication Logs | Completed |

## 3. Lynis Assessment

Lynis 3.1.7 was executed in Normal mode.

Final results:

| Metric | Result |
|---|---:|
| Tests performed | 254 |
| Hardening Index | 65 |
| Suggestions | 42 |
| Warnings | 0 |

The final scan confirmed that the vulnerable-package check and the sudoers directory permissions were OK.

## 4. Remediation

Two main remediation activities were verified:

**Sudoers permissions**

The permissions of `/etc/sudoers.d` were changed from `755` to `750`. Ownership remained `root:root`. Lynis subsequently confirmed that permissions and ownership were correct.

**Security updates**

A total of 18 packages were upgraded, including 17 standard LTS security updates. A subsequent package check showed no pending upgrades.

## 5. Manual and Automated Audit Comparison

The following comparison is based on the checks visible in the Lynis results.

| Control | Lynis coverage |
|---|---|
| C01 — System Inventory | Partial |
| C02 — Users and Groups | Partial |
| C03 — Privileged Accounts | Partial |
| C04 — Sudo Privileges | Partial |
| C05 — Critical File Permissions | Partial |
| C06 — SSH Service | Partial |
| C07 — SSH Root Login | Direct overlap |
| C08 — SSH Authentication Method | Not evidenced |
| C09 — Firewall | Partial |
| C10 — Listening Ports and Services | Partial |
| C11 — Security Updates | Partial |
| C12 — Authentication Logs | Partial |

Partial coverage means Lynis inspected a related configuration or security area but did not demonstrate the complete manual verification procedure.

## 6. Conclusion

The manual audit provided detailed verification of the 12 selected security controls. Lynis complemented this work by identifying additional security recommendations and checking system configurations automatically.

The sudoers permissions were successfully hardened and verified. Available security updates were installed, and the final Lynis scan reported no warnings.

The project completed its defined scope. The 42 remaining Lynis suggestions were not automatically applied because they were outside the selected remediation activities.

## 7. References

- CIS Ubuntu Linux 24.04 LTS Benchmark.
- ISO/IEC 27002:2022.
- Ubuntu Server documentation.
- Lynis documentation.

This project does not claim full CIS Benchmark implementation, ISO conformity, or certification.

---

**Author:** Abraham Orozco  
**Project:** Linux Security Hardening & Audit Lab
