# C12 – Authentication Logs

## Objective
Review system authentication logs and identify successful and failed login attempts.

## Audit

The following commands were used:

- `journalctl -u ssh`
- `last`
- `sudo lastb`

## Findings

The SSH logs showed successful password authentications for `abraham_orozco`.

The `last` command displayed login sessions and system reboots.

The `lastb` command showed failed login attempts from SSH and local terminal sessions.

## Result

Authentication logs were reviewed. Successful logins, login history and failed attempts were identified.

## Evidence

- `C12-01-ssh-authentication-logs.png`
- `C12-02-login-history.png`
- `C12-03-failed-login-attempts.png`
