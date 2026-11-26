# C01 — System Inventory

## Objective

Identify the main characteristics and resources of the Ubuntu Server environment used for the security assessment.

## System Information

| Component | Result |
|---|---|
| Hostname | ubuntu-auditlab |
| Operating System | Ubuntu Server 24.04.5 LTS |
| Initial Kernel | 6.8.0-149-generic |
| Kernel after security updates | 6.8.0-151-generic |
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
| sda1 | 1 MB | Partition |
| sda2 | 2 GB | Boot partition |
| sda3 | 28 GB | LVM partition |
| Root Logical Volume | 14 GB | Ubuntu root filesystem |

## Audit Commands

- `hostnamectl`
- `uname -r`
- `uname -m`
- `lscpu`
- `free -h`
- `lsblk`
- `df -h /`

## Result

The system inventory was documented successfully. The operating system, kernel, CPU, memory, virtualization platform, and storage configuration were identified.

The initial kernel version was `6.8.0-149-generic`. Following the security update process documented in C11, the system was updated to kernel version `6.8.0-151-generic`.

## Observation

The root logical volume has a capacity of 14 GB, while the virtual disk has a capacity of 30 GB. The remaining volume allocation was not investigated further as part of this control.

## Evidence

**Current system inventory after security updates:**

![C01 System Inventory](../../evidence/C01-01-system-inventory.png)
