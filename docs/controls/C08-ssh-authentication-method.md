# C08 – SSH Authentication Method

## Objective
Review the authentication methods enabled for SSH connections.

## Audit

The effective SSH configuration was checked using `sshd -T`.

## Finding

The configuration showed:

- `pubkeyauthentication yes`
- `passwordauthentication yes`

Both public key and password authentication are enabled.

## Result

The SSH server allows connections using either authentication method. No configuration changes were made.

## Evidence

- `B04-02-ssh-effective-configuration..png`
