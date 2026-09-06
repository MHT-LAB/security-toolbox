# Grafana

Dashboarding for metrics from Prometheus, Netdata, and friends — the standard visualization layer for homelab and production observability alike.

**Links:** [GitHub](https://github.com/grafana/grafana) · [Docs](https://grafana.com/docs/grafana/latest/)

## Overview

Grafana doesn't collect metrics itself — it queries a data source (Prometheus, InfluxDB, Elasticsearch) and renders dashboards. It's the visualization half of the standard "Prometheus + Grafana" monitoring pairing used everywhere from homelabs to production observability stacks.

## Install / Deploy

```bash
docker run -d -p 3000:3000 --name grafana grafana/grafana
```

## Common Commands

Web-UI driven (`http://localhost:3000`); add a data source, then build or import a dashboard (community dashboards are shareable via ID on grafana.com).

## Lab Exercise

Connect Grafana to a [Prometheus](prometheus.md) instance scraping your homelab, import a community dashboard ID for node-exporter metrics, and customize one panel to show something specific to your setup.

## Related Tools

- [Prometheus](prometheus.md) — most common data source pairing
- [Netdata](netdata.md) — can also feed Grafana, or stand alone
