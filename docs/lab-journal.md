# Laboratory Journal

## Entry 001 — Ubuntu Server Installation Troubleshooting

### Environment

| Component | Configuration |
|---|---|
| Host OS | Windows 11 |
| Hypervisor | Oracle VirtualBox |
| Guest OS | Ubuntu Server 24.04.5 LTS |
| RAM | 4 GB |
| Virtual CPUs | 2 initially, reduced to 1 |
| Virtual Disk | 30 GB |
| Network | NAT |

### Issue Observed

The virtual machine froze during Ubuntu Server installation and subsequently displayed a kernel panic.

### Investigation

Reviewed the VirtualBox configuration and system logs. NEM mode was also observed because the Windows hypervisor was active.

### Actions Taken

Reduced the virtual CPU allocation from 2 to 1 and restarted the installation.

### Result

Ubuntu Server installation continued successfully with 1 vCPU.

### Remaining Unknowns

The exact root cause of the kernel panic was not identified.
