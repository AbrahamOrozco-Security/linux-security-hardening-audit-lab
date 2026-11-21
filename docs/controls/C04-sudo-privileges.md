# C04 – Sudo Privileges

## Objective
Review the administrative privileges assigned to the user account.

## Audit

The following command was used:

```bash
sudo -l
```

## Finding

The account `abraham_orozco` has permission to execute all commands through sudo as any user or group.

The reported rule was:

```text
(ALL : ALL) ALL
```

## Result

The account has full administrative privileges through sudo. This access was identified and documented.

## Evidence

- `B03-01-permissions-and-privileges.png`
