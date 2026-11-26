# Linux Security Hardening & Audit Lab

A hands-on laboratory for manually auditing and hardening an Ubuntu Server 24.04 LTS system using native Linux command-line tools, documented evidence, and automated assessment with Lynis.

## Project Overview

This project simulates a basic server security assessment using an Ubuntu Server virtual machine.

The work included 12 manual security controls, selected hardening measures, and an independent assessment using Lynis 3.1.7 to compare automated findings with the manual audit.

## Objectives

- Audit 12 Linux security controls.
- Identify and document security weaknesses and misconfigurations.
- Apply selected hardening measures and verify their results.
- Use Lynis to perform an independent automated assessment.
- Compare manual and automated audit results.

## Laboratory Environment

| Component | Configuration |
|---|---|
| Host OS | Windows 11 |
| Virtualization | Oracle VirtualBox |
| Guest OS | Ubuntu Server 24.04.5 LTS |
| Kernel after updates | 6.8.0-151-generic |
| CPU | 1 vCPU |
| RAM | 4 GB |
| Virtual Disk | 30 GB |
| Network | NAT |
| Hostname | ubuntu-auditlab |
| Remote Administration | OpenSSH |
| Firewall | UFW |
| Automated Audit Tool | Lynis 3.1.7 |

### Remote Access

The virtual machine was administered through SSH using a VirtualBox NAT port-forwarding rule.

- Host: `127.0.0.1:2222`
- Guest: `port 22`

The host-side forwarding rule was bound to loopback.

## Manual Security Audit

The laboratory covered the following 12 controls:

| ID | Security Control | Status |
|---|---|---|
| C01 | System Inventory | Completed |
| C02 | Users and Groups | Completed |
| C03 | Privileged Accounts (UID 0) | Completed |
| C04 | Sudo Privileges | Completed |
| C05 | Critical File Permissions | Completed |
| C06 | SSH Service | Completed |
| C07 | SSH Root Login | Completed |
| C08 | SSH Authentication Method | Completed |
| C09 | Firewall | Completed |
| C10 | Listening Ports and Services | Completed |
| C11 | Security Updates | Completed |
| C12 | Authentication Logs | Completed |

Each control has an individual document in `docs/controls/` describing its objective, audit procedure, findings, result, and supporting evidence.

## Hardening and Verification

Selected security improvements were applied and verified:

- Removed unnecessary LXD group membership.
- Configured and enabled UFW while preserving SSH access.
- Restricted `/etc/sudoers.d` permissions from `755` to `750`, preserving `root:root` ownership.
- Installed 18 package updates, including 17 standard LTS security updates.
- Verified the selected changes through subsequent checks and Lynis assessments.

## Lynis Assessment Results

The final Lynis 3.1.7 assessment was performed in Normal mode.

| Metric | Final Result |
|---|---:|
| Tests performed | 254 |
| Hardening Index | 65 |
| Suggestions | 42 |
| Warnings | 0 |

The final assessment confirmed that the vulnerable-package check and `/etc/sudoers.d` permissions were OK.

The remaining suggestions were documented but not automatically applied because they were outside the selected project scope.

## Project Roadmap

| Phase | Focus | Status |
|---|---|---|
| 1 | Manual Linux Security Auditing and Hardening (12 controls) | Completed |
| 2 | Independent Automated Assessment using Lynis | Completed |
| 3 | Findings Comparison and Final Audit Report | Completed |

## Repository Structure

```text
linux-security-hardening-audit-lab/
│
├── docs/
│   ├── controls/
│   ├── lab-journal.md
│   └── final-audit-report.md
│
├── evidence/
│
└── README.md
```

## Security References

- CIS Ubuntu Linux 24.04 LTS Benchmark.
- ISO/IEC 27002:2022.
- Official Ubuntu Server documentation.
- Official Lynis documentation.

These references provide context for selected security practices. This project does not claim full CIS Benchmark implementation, formal ISO/IEC conformity, or certification.

## Disclaimer

This laboratory was conducted for educational purposes in a virtual environment owned and controlled by the author.

## Author

**Abraham Orozco**

IT Student | Cybersecurity | Cloud Security

GitHub: [AbrahamOrozco-Security](https://github.com/AbrahamOrozco-Security)
