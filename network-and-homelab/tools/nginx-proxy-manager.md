# Nginx Proxy Manager

GUI-managed reverse proxy with automatic Let's Encrypt certs — point multiple internal services at one public entry point without hand-editing nginx config.

**Links:** [GitHub](https://github.com/NginxProxyManager/nginx-proxy-manager)

## Overview

Nginx Proxy Manager gives homelab users a web UI for what used to require editing raw nginx config by hand: add a proxy host, point it at an internal service's IP:port, and it handles SSL cert issuance/renewal via Let's Encrypt automatically.

## Install / Deploy

```yaml
# docker-compose.yml
services:
  app:
    image: jc21/nginx-proxy-manager:latest
    ports: ["80:80", "81:81", "443:443"]
    volumes: ["./data:/data", "./letsencrypt:/etc/letsencrypt"]
```
```bash
docker compose up -d
```

## Common Commands

Web-UI driven at `:81`; add a Proxy Host, point it at an internal service, and request a Let's Encrypt cert with one click.

## Lab Exercise

Deploy Nginx Proxy Manager, put a homelab service (e.g. [Uptime Kuma](uptime-kuma.md)) behind it with a real domain and Let's Encrypt cert (using a domain you own), and confirm HTTPS works end to end.

## Related Tools

- [Traefik](traefik.md) — more automated, config-as-code alternative
- [Authelia](authelia.md) — add SSO in front of proxied services
