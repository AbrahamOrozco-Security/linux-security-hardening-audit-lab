# C10 – Listening Ports and Services

## Objective
Identify listening ports and services on the Ubuntu Server.

## Audit

Listening sockets and associated processes were reviewed using `ss`.

## Finding

The review identified:

- TCP 22: SSH, listening on IPv4 and IPv6 interfaces.
- TCP/UDP 53: DNS service, listening on loopback.
- UDP 68: DHCP client service.

## Result

The listening services were identified and reviewed alongside the firewall configuration. SSH connectivity was verified after hardening.

## Evidence

- B05 listening sockets screenshot.
- B05 post-hardening network verification.
