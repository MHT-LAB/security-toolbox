# Traefik

Cloud-native reverse proxy/load balancer with automatic service discovery — detects new containers automatically and configures routing without manual entry per service.

**Links:** [GitHub](https://github.com/traefik/traefik) · [Docs](https://doc.traefik.io/traefik/)

## Overview

Where Nginx Proxy Manager is GUI-first, Traefik is config-as-code and container-aware — label a Docker container with routing rules, and Traefik picks it up automatically without a separate manual "add proxy host" step. Better suited once you're comfortable with Docker labels/YAML.

## Install / Deploy

```yaml
# docker-compose.yml
services:
  traefik:
    image: traefik:v3.0
    command: ["--providers.docker=true", "--entrypoints.web.address=:80"]
    ports: ["80:80"]
    volumes: ["/var/run/docker.sock:/var/run/docker.sock"]
```

## Common Commands

```yaml
# on any other container, add labels:
labels:
  - "traefik.http.routers.myapp.rule=Host(`myapp.local`)"
```

## Lab Exercise

Deploy Traefik alongside two labeled homelab services and confirm both route correctly by hostname with zero manual proxy-host configuration — then compare the experience against [Nginx Proxy Manager](nginx-proxy-manager.md)'s GUI-driven approach for the same task.

## Related Tools

- [Nginx Proxy Manager](nginx-proxy-manager.md) — GUI-first alternative
