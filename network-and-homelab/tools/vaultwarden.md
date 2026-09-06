# Vaultwarden

Lightweight self-hosted Bitwarden-compatible password manager server — same client apps as official Bitwarden, much lower resource footprint on the server side.

**Links:** [GitHub](https://github.com/dani-garcia/vaultwarden)

## Overview

Vaultwarden implements the Bitwarden server API in Rust, meaning every official Bitwarden client (browser extension, mobile app, desktop app) works against it unmodified — a popular choice for homelabbers who want Bitwarden's ecosystem without the official server's resource requirements.

## Install / Deploy

```bash
docker run -d --name vaultwarden -p 8080:80 -v ./vw-data:/data vaultwarden/server:latest
```

## Common Commands

Managed via the Bitwarden web vault UI and official client apps pointed at your self-hosted server URL.

## Lab Exercise

Deploy Vaultwarden behind [Nginx Proxy Manager](nginx-proxy-manager.md) with a real HTTPS cert, connect the official Bitwarden browser extension to it, and confirm sync works end to end before relying on it for real credentials.

## Related Tools

- [Nginx Proxy Manager](nginx-proxy-manager.md) · [Traefik](traefik.md) — needed in front for HTTPS
- [Authelia](authelia.md) — complementary SSO layer for other services
