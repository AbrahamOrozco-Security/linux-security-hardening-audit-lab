# C03 – Privileged Accounts (UID 0)

## Objective
Identify accounts with UID 0 on the Ubuntu Server.

## Audit

I used the following command to list account names and their UIDs:

```bash
getent passwd | cut -d: -f1,3
```

## Finding

The audit identified `root` as the only account with UID 0. No other accounts with root-level UID privileges were found.

## Result

The UID 0 account configuration was reviewed. No additional privileged accounts were identified.

## Evidence

- `C03-01-uid-zero-accounts.png`
