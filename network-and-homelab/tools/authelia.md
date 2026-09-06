# Authelia

Self-hosted SSO/2FA authentication portal for reverse-proxied services — adds a login/2FA gate in front of services that don't have their own auth.

**Links:** [GitHub](https://github.com/authelia/authelia) · [Docs](https://www.authelia.com/overview/prologue/introduction/)

## Overview

Many self-hosted homelab tools (dashboards, monitoring UIs) have weak or no built-in authentication. Authelia sits in front of them via your reverse proxy, providing a single login (with 2FA) that gates access to everything behind it.

## Install / Deploy

```bash
docker run -d -p 9091:9091 -v ./config:/config authelia/authelia
# Requires reverse-proxy integration (nginx/Traefik) with forward-auth configured
```

## Common Commands

Configuration is YAML-based (`configuration.yml`); day-to-day use is the login portal itself.

## Lab Exercise

Put Authelia in front of a homelab dashboard with no built-in login (e.g. [Uptime Kuma](uptime-kuma.md)'s status page) via [Traefik](traefik.md)'s forward-auth middleware, and confirm you're prompted for 2FA before reaching it.

## Related Tools

- [Authentik](authentik.md) · [Keycloak](keycloak.md) — heavier full-IdP alternatives
- [Traefik](traefik.md) · [Nginx Proxy Manager](nginx-proxy-manager.md) — required reverse-proxy layer
