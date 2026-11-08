# C01 — System Inventory

## Objective

Identify the main characteristics and resources of the Ubuntu Server before performing security audits.

## System Information

| Component | Result |
|---|---|
| Hostname | ubuntu-auditlab |
| Operating System | Ubuntu Server 24.04.5 LTS |
| Kernel | 6.8.0-149-generic |
| Architecture | x86_64 |
| Virtualization | Oracle VirtualBox |
| CPU Model | Intel Core i7-14650HX |
| Assigned CPUs | 1 vCPU |
| RAM | 4 GB |
| Virtual Disk | 30 GB |
| Root Filesystem | 14 GB |

## Storage Information

| Device | Size | Description |
|---|---|---|
| sda | 30 GB | Virtual disk |
| sda2 | 2 GB | Boot partition |
| sda3 | 28 GB | LVM partition |
| Root Logical Volume | 14 GB | Ubuntu root filesystem |

## Audit Commands

- `hostnamectl`
- `uname -r`
- `uname -m`
- `uptime`
- `free -h`
- `df -h /`
- `lsblk`
- `lscpu`

## Result

The initial system inventory was completed successfully. The operating system, kernel, CPU, memory and storage configuration were identified.

## Observation

The root logical volume has a capacity of 14 GB, while the virtual disk has a capacity of 30 GB. The remaining volume allocation requires further inspection.
