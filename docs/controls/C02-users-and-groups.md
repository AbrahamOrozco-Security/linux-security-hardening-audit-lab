# C02 – Users and Groups

## Objective
Review the user accounts and groups configured on the Ubuntu Server.

## Audit

The account `abraham_orozco` was reviewed.

| Attribute | Value |
|---|---|
| UID | 1000 |
| Primary group | abraham_orozco |
| Home directory | /home/abraham_orozco |
| Shell | /bin/bash |

The account initially belonged to these groups:

- adm
- cdrom
- sudo
- dip
- plugdev
- lxd

## Finding and Action

The user was a member of the `lxd` group, although LXD was not used.

I removed the account from this group using:

```bash
sudo gpasswd -d abraham_orozco lxd
```

## Verification

The following checks confirmed the change:

- `getent group lxd`: the group no longer lists the user.
- `id abraham_orozco`: the account no longer belongs to `lxd`.
- Membership in `sudo` remains unchanged.

## Result

The unnecessary `lxd` membership was removed. The account's group membership was verified.

## Evidence

## Evidence

- `C02-01-user-account-enumeration.png`
- `C02-02-user-group-memberships.png`
