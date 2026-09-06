# Prometheus

The standard open-source metrics collection and alerting engine — pulls (scrapes) metrics from configured targets on an interval and stores them as time series.

**Links:** [GitHub](https://github.com/prometheus/prometheus) · [Docs](https://prometheus.io/docs/introduction/overview/)

## Overview

Prometheus scrapes metrics endpoints (exposed by exporters like `node_exporter`, or natively by many applications) on a schedule, stores them as time series, and evaluates alerting rules against them — Grafana then visualizes what Prometheus collects.

## Install / Deploy

```bash
docker run -d -p 9090:9090 -v ./prometheus.yml:/etc/prometheus/prometheus.yml \
  prom/prometheus
```

## Common Commands

```yaml
# prometheus.yml
scrape_configs:
  - job_name: 'node'
    static_configs:
      - targets: ['localhost:9100']
```
```text
# PromQL query example, in the web UI:
rate(node_cpu_seconds_total[5m])
```

## Lab Exercise

Deploy `node_exporter` on a lab VM, configure Prometheus to scrape it, and write a basic PromQL query for CPU usage — then connect [Grafana](grafana.md) to visualize it.

## Related Tools

- [Grafana](grafana.md) — the standard visualization pairing
- [Netdata](netdata.md) — zero-config alternative for single-host monitoring
