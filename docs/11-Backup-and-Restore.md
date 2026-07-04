# Backup and Restore

## Overview

Backups ensure that data can be recovered after hardware failure, accidental deletion, or corruption.

The project uses Nextcloud AIO's built-in backup capabilities together with planned external storage.

---

# Backup Strategy

Current storage:

```
D:\CloudServer\Data
```

Recommended backup location:

```
D:\CloudServer\Backups
```

Future option:

```
N:\NextcloudBackups
```

---

# Backup Types

## Configuration

Includes:

- Nextcloud settings
- Installed apps
- User configuration

---

## Database

Includes:

- User accounts
- Shares
- Metadata
- Settings

---

## User Data

Includes:

- Uploaded files
- Photos
- Documents
- Videos

---

# Backup Schedule

Recommended:

| Frequency | Type |
|-----------|------|
| Daily | Incremental |
| Weekly | Full |
| Monthly | Archive |

---

# Backup Workflow

```mermaid
flowchart LR

Nextcloud

-->

Backup Process

-->

Backup Folder

-->

External Drive

-->

Cloud Storage (Optional)
```

---

# Restore Procedure

General steps:

1. Stop Nextcloud containers.
2. Verify backup integrity.
3. Restore data and database.
4. Start containers.
5. Verify user access.

---

# Best Practices

- Test restores regularly.
- Keep multiple backup copies.
- Store backups on a different physical device.
- Follow the 3-2-1 backup strategy:
  - 3 copies of your data
  - 2 different storage media
  - 1 copy off-site

---

# Planned Automation

PowerShell scripts:

```
backup.ps1
restore.ps1
update.ps1
```

These scripts will automate routine maintenance and backup operations.

---

# Lessons Learned

Backups are only valuable if they can be successfully restored. Periodic restore testing is an essential part of any backup strategy.