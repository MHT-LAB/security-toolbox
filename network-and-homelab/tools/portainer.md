# Portainer CE

Free Docker/container management UI — see and manage containers, images, volumes, and stacks without living in the CLI.

**Links:** [GitHub](https://github.com/portainer/portainer) · [Docs](https://docs.portainer.io)

## Overview

Portainer gives Docker (and Kubernetes/Swarm) a web UI for the day-to-day operations — start/stop containers, view logs, deploy a docker-compose stack — useful once a homelab has more than a couple of containers to keep track of via `docker ps` alone.

## Install / Deploy

```bash
docker volume create portainer_data
docker run -d -p 8000:8000 -p 9443:9443 --name portainer --restart=always \
  -v /var/run/docker.sock:/var/run/docker.sock \
  -v portainer_data:/data portainer/portainer-ce:latest
```

## Common Commands

Portainer is web-UI driven (`https://localhost:9443`); deploy stacks via the Stacks section using standard docker-compose YAML.

## Lab Exercise

Deploy Portainer, then use its Stacks feature to deploy [Uptime Kuma](uptime-kuma.md) or [Pi-hole](pi-hole.md) from a docker-compose snippet, and compare the experience against running the same `docker run` command by hand.

## Related Tools

- Nearly every self-hosted service in this folder can be deployed/managed through it
