# C11 – Security Updates

## Objective
Check for available security updates and verify package maintenance.

## Audit

The following commands were used:

- `sudo apt update`
- `apt list --upgradable`
- `sudo apt upgrade`
- `uname -r`

## Finding

Initially, 61 packages had updates available. The upgrade process installed 61 updates and 7 new packages, including 16 standard LTS security updates.

A new kernel version was installed: `6.8.0-151-generic`.

## Result

The server was rebooted and the new kernel was verified. A final package check showed no pending updates.

## Evidence

## Evidence

- `C11-02-updates-after-upgrade (2).png`

The initial pending updates and package upgrade results are documented in the audit findings. A separate screenshot of the initial package listing is not included in the repository evidence.
