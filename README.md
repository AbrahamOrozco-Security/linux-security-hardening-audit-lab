# Linux Security Hardening & Audit Lab

A hands-on laboratory for auditing and hardening an Ubuntu Server 24.04 LTS system using Bash, with documented evidence and before/after verification.

## Project Overview

This project simulates a real server administration environment using an Ubuntu Server virtual machine. I audit a defined set of 12 security controls, document findings with evidence, apply remediations in a controlled way, and re-audit to verify the results.

Some lab scenarios introduce weaknesses **intentionally** (after taking a VM snapshot) so that detection and remediation can be tested. Every intentional weakness is documented as such.

## Objectives

- Audit 12 Linux security controls on Ubuntu Server 24.04 LTS (identity, privileges, SSH, firewall, services, updates, logs).
- Build Bash scripts that automate each check and save timestamped evidence.
- Document every control with its risk, evidence, result, remediation and re-test.
- Apply remediations using VM snapshots so every "before" state is reproducible.
- Cross-check my results against Lynis to see what my checks miss.
- Relate each control to CIS Benchmark and ISO/IEC 27002 references.

## Laboratory Architecture

| Component | Technology |
|---|---|
| Host operating system | Windows 11 |
| Virtualization | Oracle VirtualBox |
| Guest operating system | Ubuntu Server 24.04.5 LTS |
| Remote administration | OpenSSH |
| Administration terminal | Windows PowerShell |
| Scripting | Bash |
| Version control | Git and GitHub |

### Virtual Machine

| Resource | Value |
|---|---|
| vCPU | 1 |
| RAM | 4 GB |
| Disk | 30 GB (dynamic) |
| Network | NAT |
| Hostname | ubuntu-auditlab |

### Remote Access

The VM is administered over SSH through a VirtualBox NAT port-forwarding rule.

- Host side: `127.0.0.1:2222` (loopback only, not exposed to the local network)
- Guest side: port `22` (OpenSSH)

## Audit Scope: 12 Controls

| ID | Control | Status |
|---|---|---|
| C01 | System inventory | Planned |
| C02 | Users and groups | Planned |
| C03 | Privileged accounts (UID 0) | Planned |
| C04 | Sudo privileges | Planned |
| C05 | Critical file permissions | Planned |
| C06 | SSH service | Planned |
| C07 | SSH root login | Planned |
| C08 | SSH authentication method | Planned |
| C09 | Firewall | Planned |
| C10 | Listening ports and services | Planned |
| C11 | Security updates | Planned |
| C12 | Authentication logs | Planned |

Each control gets its own sheet: objective, risk, procedure, evidence, result, recommendation, re-test and references.

## Audit Methodology

1. **Audit:** Inspect system configurations and security settings.
2. **Identify:** Detect potential weaknesses and misconfigurations.
3. **Document:** Record findings and supporting evidence.
4. **Remediate:** Apply a hardening measure after taking a snapshot.
5. **Verify:** Re-run the check to confirm the change.
6. **Compare:** Evaluate the system before and after remediation.

## Repository Structure

Planned layout (folders will be added as the project grows):

- `docs/` architecture, methodology and lab journal
- `docs/controls/` individual control documentation
- `scripts/audit/` Bash security audit modules
- `scripts/hardening/` hardening procedures
- `evidence/` saved command output and supporting evidence
- `reports/` audit reports and before/after comparisons

## Lab Journal

My working notes live in `docs/lab-journal.md` (coming soon).

## Troubleshooting Log

**Ubuntu Server installation encountered errors with 2 vCPUs.**

After reviewing VirtualBox logs and reducing the VM allocation to 1 vCPU, the installation proceeded successfully. The root cause has not been conclusively identified; details will be added to the lab journal.

## Project Roadmap

| Phase | Focus | Status |
|---|---|---|
| 1 | Linux and Bash security auditing | In progress |
| 2 | AWS cloud security laboratory | Planned |
| 3 | Python-based audit automation | Planned |
| 4 | Infrastructure as Code with Terraform | Planned |

## Current Progress

- [x] Ubuntu Server 24.04.5 LTS installed.
- [x] VirtualBox laboratory configured.
- [x] OpenSSH server installed and enabled.
- [x] Remote SSH access verified from Windows PowerShell.
- [ ] Snapshot `00-clean-install` created.
- [ ] Initial system baseline.
- [ ] Bash audit modules (C01-C12).
- [ ] Remediation and re-audit.
- [ ] Comparison with Lynis.
- [ ] Final audit report.

## Security References

- CIS Ubuntu Linux 24.04 LTS Benchmark
- ISO/IEC 27002:2022
- Ubuntu Server documentation

These references guide individual checks where applicable. This project does not claim certification or compliance with any standard.

## Disclaimer

This laboratory is for educational purposes and was performed in an isolated environment that I own and control.

## Author

**Abraham Orozco**

IT Student | Cybersecurity | Cloud Security

GitHub: [AbrahamOrozco-Security](https://github.com/AbrahamOrozco-Security)
