# Uptime Kuma

Self-hosted uptime monitoring with a clean dashboard — the simplest way to get "is this service actually up" alerting for a homelab.

**Links:** [GitHub](https://github.com/louislam/uptime-kuma)

## Overview

Uptime Kuma monitors HTTP(S), TCP, ping, and DNS targets on an interval, showing uptime history and response-time graphs, with notification integrations (email, Slack, Discord, and dozens more) when something goes down.

## Install / Deploy

```bash
docker run -d --restart=always -p 3001:3001 \
  -v uptime-kuma:/app/data --name uptime-kuma louislam/uptime-kuma:1
```

## Common Commands

Web-UI driven at `http://localhost:3001`; add monitors and notification channels through the dashboard.

## Lab Exercise

Add monitors for every self-hosted service in your homelab (Pi-hole, TrueNAS, your Wazuh manager), configure a Discord/email notification, then stop one service manually and confirm the alert actually fires.

## Related Tools

- [Netdata](netdata.md) — deeper performance-metrics complement
- [Grafana](grafana.md) · [Prometheus](prometheus.md) — heavier alternative for custom dashboards
