# Docker Volumes

## Overview

Docker volumes store persistent data independently from containers.

Deleting a container does **not** delete its associated volume.

---

## Why Volumes?

Benefits

- Data persistence
- Easier upgrades
- Safer container recreation
- Backup support

---

## Volumes Used

### nextcloud_aio_mastercontainer

Stores

- AIO configuration
- Passphrase
- Deployment settings

---

### nextcloud_aio_database

Stores PostgreSQL database.

---

### nextcloud_aio_database_dump

Stores database backups.

---

### nextcloud_aio_nextcloud

Stores application files.

---

### nextcloud_aio_nextcloud_data

Stores uploaded user data (if not using `NEXTCLOUD_DATADIR`).

---

### nextcloud_aio_redis

Stores Redis persistence.

---

## List Volumes

```powershell
docker volume ls
```

---

## Inspect Volume

```powershell
docker volume inspect nextcloud_aio_mastercontainer
```

---

## Remove Volume

```powershell
docker volume rm VOLUME_NAME
```

⚠️ Removing a volume permanently deletes the stored data.

---

## Best Practices

- Never remove volumes unless intentionally resetting the deployment.
- Keep backups before making storage changes.
- Use host-mounted storage for large datasets.
- Separate backups from live data.

---

## Volume Relationships

```mermaid
flowchart TD

Docker

-->

Master Volume

Docker

-->

Database Volume

Docker

-->

Redis Volume

Docker

-->

Nextcloud Volume

Nextcloud

-->

D:\\CloudServer\\Data
```