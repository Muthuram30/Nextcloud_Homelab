# System Requirements

## Hardware Requirements

| Component | Recommended |
|-----------|-------------|
| CPU | 4 Cores |
| RAM | 8 GB or higher |
| Storage | 100 GB+ SSD |
| Internet | Stable broadband |
| External Storage | Optional USB HDD |

---

# Software Requirements

| Software | Version |
|----------|---------|
| Windows | 11 |
| Docker Desktop | Latest |
| Nextcloud AIO | Latest |
| PowerShell | 7+ (Recommended) |
| Git | Latest |

---

# Network Requirements

- Internet Connection
- Cloudflare Account
- Registered Domain
- HTTPS Support

---

# Docker Requirements

Docker Desktop must support:

- Linux Containers
- Docker Volumes
- Docker Networking
- WSL2 Backend

Verify installation:

```powershell
docker version
```

Verify engine:

```powershell
docker ps
```

---

# Storage Planning

Internal Storage

```
D:\CloudServer

├── Data
├── Backups
└── Logs
```

Future External Storage

```
N:\NextcloudExternal
```

---

# Security Requirements

- HTTPS only
- Strong passwords
- Cloudflare Tunnel
- Administrator account
- Regular updates

---

# Browser Compatibility

- Microsoft Edge
- Google Chrome
- Firefox
- Safari

---

# Domain Requirements

Example:

```
cloud.myservs.in
```

Must resolve through Cloudflare.