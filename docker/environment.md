# Environment Variables

## Overview

Environment variables customize the behaviour of the Nextcloud AIO deployment.

---

## APACHE_PORT

```text
11000
```

Purpose:

The internal Apache container listens on this port.

Cloudflare Tunnel forwards requests to this port.

---

## APACHE_IP_BINDING

```text
0.0.0.0
```

Purpose:

Allows Apache to listen on all interfaces inside Docker.

---

## NEXTCLOUD_DATADIR

```text
/run/desktop/mnt/host/d/CloudServer/Data
```

Purpose:

Stores all uploaded user files outside Docker containers.

Benefits

- Persistent storage
- Easy backup
- Easier migration
- Better organization

---

## NEXTCLOUD_MOUNT

```text
/run/desktop/mnt/host/n/NextcloudExternal
```

Purpose

Allows removable external storage to appear inside Nextcloud.

---

## Docker Socket

```text
/run/host-services/docker.proxy.sock
```

Purpose

Allows the AIO master container to control Docker containers.

---

## Summary

| Variable | Purpose |
|-----------|---------|
| APACHE_PORT | Internal web server |
| APACHE_IP_BINDING | Apache binding |
| NEXTCLOUD_DATADIR | Persistent storage |
| NEXTCLOUD_MOUNT | External storage |