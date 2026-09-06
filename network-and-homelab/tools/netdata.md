# Netdata

Real-time infrastructure and performance monitoring — per-second granularity metrics with zero-configuration auto-discovery of what to monitor.

**Links:** [GitHub](https://github.com/netdata/netdata) · [Docs](https://learn.netdata.cloud)

## Overview

Netdata auto-detects services running on a host (databases, web servers, containers) and immediately starts graphing detailed per-second metrics, with almost no configuration needed — a fast way to get deep visibility into a single host without building Prometheus/Grafana dashboards from scratch.

## Install / Deploy

```bash
curl -Ss https://get.netdata.cloud/kickstart.sh | sh
```

## Common Commands

Netdata is web-UI driven (`http://localhost:19999`) with real-time auto-updating charts; no query language needed for basic use.

## Lab Exercise

Install Netdata on a lab VM running a few services (a database, a web server), and use its auto-generated dashboards to identify which process is consuming the most CPU/memory during a load test.

## Related Tools

- [Uptime Kuma](uptime-kuma.md) — simpler up/down monitoring complement
- [Grafana](grafana.md) · [Prometheus](prometheus.md) — for building custom long-term dashboards
