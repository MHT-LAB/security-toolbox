# Docker Compose

The standard way most of this list actually gets deployed in a homelab — define a multi-container stack in one YAML file and bring it up/down as a unit.

**Links:** [GitHub](https://github.com/docker/compose) · [Docs](https://docs.docker.com/compose/)

## Overview

Nearly every self-hosted tool in this repo ships a `docker-compose.yml` as its recommended deployment method — Compose defines services, networks, and volumes together, so a whole stack (app + database + reverse proxy) comes up with one `docker compose up`.

## Install / Deploy

```bash
# Bundled with modern Docker installs as the `docker compose` subcommand.
docker compose version
```

## Common Commands

```bash
docker compose up -d
docker compose logs -f <service>
docker compose down
```

## Lab Exercise

Write a docker-compose.yml from scratch for a two-service stack (e.g. [Pi-hole](pi-hole.md) plus [Uptime Kuma](uptime-kuma.md) monitoring it), bring it up, and confirm both services start correctly and can see each other on the Compose-created network.

## Related Tools

- [Portainer CE](portainer.md) — GUI for managing Compose stacks
