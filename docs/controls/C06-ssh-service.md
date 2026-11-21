# C06 – SSH Service

## Objective
Review the SSH service status and startup configuration.

## Audit

The service was reviewed using:

```bash
systemctl status ssh
```

## Finding

The SSH service was active and running. It was also enabled to start automatically at boot.

## Result

The SSH service is operational and configured to start automatically.

## Evidence

- SSH service status screenshot.
- SSH listening port screenshot (port 22).
