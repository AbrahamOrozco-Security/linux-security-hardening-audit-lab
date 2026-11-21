# C05 – Critical File Permissions

## Objective
Review the permissions and ownership of critical system files.

## Audit

The following command was used:

```bash
sudo ls -l /etc/passwd /etc/shadow /etc/group /etc/gshadow
```

## Results

| File | Permissions | Owner |
|---|---|---|
| /etc/passwd | 644 | root:root |
| /etc/shadow | 640 | root:shadow |
| /etc/group | 644 | root:root |
| /etc/gshadow | 640 | root:shadow |

## Finding

The four files have the expected ownership and permission settings. No unexpected permissions were identified during this review.

## Result

The permissions and ownership of the selected critical files were reviewed. No changes were necessary.

## Evidence

- `C05-01-critical-file-permissions.png`
