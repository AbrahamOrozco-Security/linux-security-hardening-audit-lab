# C09 – Firewall

## Objective
Review and configure the system firewall.

## Audit

UFW was initially inactive. The firewall was configured with the following rules:

- Incoming traffic: denied by default.
- Outgoing traffic: allowed.
- SSH: allowed on TCP port 22.
- Logging: enabled.

## Result

UFW was enabled and its configuration was verified. SSH connectivity remained functional after hardening.

## Evidence

- B05 firewall baseline screenshot.
- B05 UFW enable confirmation.
- B05 post-hardening verification.
