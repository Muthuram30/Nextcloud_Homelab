# DNS Configuration

## Overview

To provide a professional and memorable URL, I configured a custom subdomain using Cloudflare DNS.

Example:

```
cloud.myservs.in
```

---

# DNS Flow

```mermaid
flowchart LR

Browser

-->

Cloudflare DNS

-->

Cloudflare Tunnel

-->

Docker

-->

Nextcloud
```

---

# Steps Performed

1. Registered domain.
2. Added domain to Cloudflare.
3. Updated nameservers.
4. Created a Tunnel.
5. Added a Public Hostname.

---

# Public Hostname

Hostname

```
cloud.myservs.in
```

Service

```
HTTP
```

URL

```
http://host.docker.internal:11000
```

---

# HTTPS

Cloudflare automatically provides TLS encryption.

Users access:

```
https://cloud.myservs.in
```

No certificates needed on the home server.

---

# Verification

DNS lookup:

```powershell
nslookup cloud.myservs.in
```

Browser:

```
https://cloud.myservs.in
```

---

# Best Practices

- Use HTTPS only
- Keep DNS managed through Cloudflare
- Do not expose Docker ports publicly
- Keep Tunnel token private