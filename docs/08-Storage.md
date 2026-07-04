# Storage Configuration

## Overview

Persistent storage is essential because Docker containers are ephemeral.

Instead of storing user data inside containers, Nextcloud stores data on the host machine.

---

# Initial Storage

Originally, Docker volumes handled storage.

Later, the data directory was migrated.

---

# Final Directory

```
D:\CloudServer

├── Data
├── Backups
└── Logs
```

---

# Environment Variable

```powershell
-e NEXTCLOUD_DATADIR=/run/desktop/mnt/host/d/CloudServer/Data
```

---

# Why Persistent Storage?

Benefits:

- Survives container recreation
- Easier backup
- Easier migration
- Better organization

---

# Storage Flow

```mermaid
flowchart TD

Nextcloud

-->

Docker

-->

Host Storage

-->

D:\CloudServer\Data
```

---

# External Storage Planning

Planned configuration:

```
N:\NextcloudExternal
```

Using:

```powershell
-e NEXTCLOUD_MOUNT=/run/desktop/mnt/host/n/NextcloudExternal
```

This allows removable storage while keeping the main cloud data on the internal drive.

---

# Lessons Learned

Changing `NEXTCLOUD_DATADIR` after Nextcloud has already been initialized is not supported.

The correct approach is to decide the storage location before the first deployment or perform a clean installation if changing it later.

---

# Best Practices

- Store live data on a reliable internal drive.
- Keep backups separate from live data.
- Assign a permanent drive letter to removable drives.
- Stop containers before disconnecting external storage.