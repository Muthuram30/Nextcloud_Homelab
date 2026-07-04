# Installation

## Overview

The deployment begins by preparing the Windows environment and installing Docker Desktop.

---

# Step 1

Install Docker Desktop.

Official Website:

https://www.docker.com/products/docker-desktop/

---

# Step 2

Enable:

- WSL2 Backend
- Linux Containers

---

# Step 3

Restart the computer.

---

# Step 4

Verify Docker.

```powershell
docker version
```

Example output:

```
Client:
 Version: xx.xx.xx

Server:
 Engine: xx.xx.xx
```

---

# Step 5

Verify Docker Engine.

```powershell
docker ps
```

Expected:

```
CONTAINER ID
IMAGE
COMMAND
```

No errors should appear.

---

# Step 6

Pull the latest Nextcloud image.

```powershell
docker pull nextcloud/all-in-one:latest
```

---

# Installation Checklist

- Docker Installed

- Docker Running

- WSL2 Enabled

- Internet Working

- Domain Purchased

- Cloudflare Account Created

---

# Notes

Docker Desktop must remain running while Nextcloud is in use.