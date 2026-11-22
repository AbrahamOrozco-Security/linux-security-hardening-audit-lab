# Linux Security Hardening & Audit Lab

A hands-on laboratory for manually auditing and hardening an Ubuntu Server 24.04 LTS system using native Linux command-line tools, with documented evidence and before-and-after verification.

## Project Overview

This project simulates a server security assessment environment using an Ubuntu Server virtual machine.

The laboratory focuses on manually auditing 12 defined Linux security controls, identifying potential weaknesses, documenting findings and supporting evidence, applying appropriate security hardening measures, and verifying the results.

An independent security assessment using Lynis will also be performed to compare automated findings against the manual audit and identify potential gaps in the assessment process.

## Objectives

- Perform a manual security audit of 12 Linux security controls covering identities, privileges, SSH, firewall, services, updates, and authentication logs.
- Inspect system configurations using native Linux command-line utilities.
- Document each control, including its objective, audit procedure, findings, risk, evidence, remediation, and verification.
- Apply appropriate security hardening measures and verify configuration changes.
- Use Lynis as an independent automated security assessment tool and compare its findings against the manual audit.
- Consult relevant CIS Benchmark and ISO/IEC 27002 references to contextualize selected security practices.

## Laboratory Architecture

| Component | Technology |
|---|---|
| Host operating system | Windows 11 |
| Virtualization | Oracle VirtualBox |
| Guest operating system | Ubuntu Server 24.04.5 LTS |
| Remote administration | OpenSSH |
| Administration terminal | Windows PowerShell |
| Command-line shell | Bash |
| Version control | Git and GitHub |

## Virtual Machine

| Resource | Value |
|---|---|
| vCPU | 1 |
| RAM | 4 GB |
| Disk | 30 GB (dynamic) |
| Network | NAT |
| Hostname | ubuntu-auditlab |

## Remote Access

The virtual machine is administered over SSH through a VirtualBox NAT port-forwarding rule.

- Host side: `127.0.0.1:2222` (loopback only, not exposed to the local network).
- Guest side: port `22` (OpenSSH).

## Audit Scope: 12 Security Controls

| ID | Control | Status |
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

Each control has an individual document describing its objective, audit procedure, findings, results, and supporting evidence.

## Audit Methodology

The laboratory follows a structured security assessment process:

1. **Audit:** Inspect system configurations and security settings.
2. **Identify:** Detect potential weaknesses and misconfigurations.
3. **Document:** Record findings, risks, and supporting evidence.
4. **Remediate:** Apply appropriate security hardening measures when necessary.
5. **Verify:** Re-examine the system to confirm configuration changes.
6. **Compare:** Evaluate the system before and after selected remediation activities.

VM snapshots are used as recovery points before selected security changes.

## Repository Structure

```text
linux-security-hardening-audit-lab/
│
├── docs/
│   ├── controls/
│   └── lab-journal.md
│
├── evidence/
│
└── README.md
```

## Lab Journal

Laboratory activities, technical observations, and learning progress are documented in `docs/lab-journal.md`.

## Project Roadmap

| Phase | Focus | Status |
|---|---|---|
| 1 | Manual Linux Security Auditing and Hardening (12 controls) | Completed |
| 2 | Independent Automated Security Assessment using Lynis | Planned |
| 3 | Findings Comparison and Final Audit Report | Planned |

## Current Progress

### Infrastructure

- [x] Ubuntu Server 24.04.5 LTS installed.
- [x] VirtualBox laboratory configured.
- [x] OpenSSH server installed and enabled.
- [x] Remote SSH access verified from Windows PowerShell.
- [x] Snapshot `00-clean-install` created.
- [x] Snapshot `01-pre-firewall-hardening` created.

### Learning Progress

- [x] Block 1 — System Inventory.
- [x] Block 2 — Identities and Privileges.
- [x] Block 3 — Permissions and Administration.
- [x] Block 4 — SSH Service and Access.
- [x] Block 5 — Network Exposure.
- [x] Block 6 — Maintenance and Logs.

### Security Audit Results

- [x] C01 — System Inventory documented.
- [x] C02 — Users and Groups: account and group memberships reviewed; unnecessary LXD membership removed and verified.
- [x] C03 — Privileged Accounts (UID 0): root confirmed as the only account with UID 0.
- [x] C04 — Sudo Privileges: administrative permissions reviewed and documented.
- [x] C05 — Critical File Permissions: ownership and permissions of four critical system files reviewed; no changes required.
- [x] C06 — SSH Service: service status and automatic startup reviewed and documented.
- [x] C07 — SSH Root Login: effective root login configuration reviewed and documented.
- [x] C08 — SSH Authentication Method: password and public key authentication settings reviewed and documented.
- [x] C09 — Firewall: UFW configured, enabled, and verified; SSH connectivity maintained after hardening.
- [x] C10 — Listening Ports and Services: listening ports and services reviewed before and after firewall configuration.
- [x] C11 — Security Updates: 61 packages upgraded, including 16 standard LTS security updates; new kernel verified and no pending updates remained at the time of the audit.
- [x] C12 — Authentication Logs: SSH authentication events, login history, and failed login attempts reviewed and documented.

### Remaining Project Activities

- [ ] Install and execute Lynis for an independent system security assessment.
- [ ] Review and interpret Lynis findings, warnings, and recommendations.
- [ ] Compare Lynis results against the 12 manually audited security controls.
- [ ] Identify assessment gaps and evaluate additional security recommendations.
- [ ] Prepare the consolidated final audit report.

## Security References

- CIS Ubuntu Linux 24.04 LTS Benchmark (v2.0.0).
- ISO/IEC 27002:2022.
- Official Ubuntu Server documentation.
- Official Lynis documentation.

These references provide context for selected security practices and future assessment activities. The laboratory does not represent a complete CIS Benchmark implementation, formal ISO/IEC conformity assessment, or certification. Specific control mappings will only be claimed when individually reviewed and documented.

## Disclaimer

This laboratory is for educational purposes and was performed in an isolated environment owned and controlled by the author.

## Author

**Abraham Orozco**

IT Student | Cybersecurity | Cloud Security

GitHub: AbrahamOrozco-Security
