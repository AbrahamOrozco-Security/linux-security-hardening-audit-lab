# C02 – User and Group Enumeration

## Objective
Identify the user accounts registered in the Ubuntu Server system.

## Command
```bash
getent passwd | cut -d: -f1
```

## Command Description
- `getent passwd`: retrieves account information from the system's configured user database.
- `cut -d: -f1`: extracts the first field, using the colon (`:`) as the delimiter. This field contains the username.

## Observation
The command displays the registered system and regular user accounts, including `root`, service accounts, and `abraham_orozco`.

## Result
User account enumeration successfully performed.

## Evidence
`evidence/C02-01-user-account-enumeration.png`
