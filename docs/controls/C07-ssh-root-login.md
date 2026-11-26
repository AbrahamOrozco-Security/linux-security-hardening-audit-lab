# C07 – SSH Root Login

## Objective
Check whether direct root login is allowed through SSH.

## Audit

The effective SSH configuration was reviewed using `sshd -T`.

## Finding

The setting `PermitRootLogin` was configured as `without-password`.

This means root login using a password is disabled, while public-key authentication remains allowed.

## Result

Root password authentication is restricted. No configuration changes were made.

## Evidence

- `B04-02-ssh-effective-configuration..png`
