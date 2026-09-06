# Graylog

Centralized log management with a free tier that scales further than most homelabs need — collects, indexes, and searches logs from anywhere you can point a syslog/GELF feed.

**Links:** [GitHub](https://github.com/Graylog2/graylog2-server) · [Docs](https://go2docs.graylog.org)

## Overview

Graylog centralizes logs (syslog, GELF, or custom inputs) into an Elasticsearch-backed searchable index with dashboards and alerting rules — a lighter alternative to standing up the full Elastic Stack yourself when you mainly need log search and basic alerting.

## Install / Deploy

```bash
# Official docker-compose stack (Graylog + MongoDB + Elasticsearch):
git clone https://github.com/Graylog2/docker-compose.git
cd docker-compose && docker-compose up
```

## Common Commands

Graylog is web-UI driven; log search uses Lucene-style syntax:
```text
source:webserver01 AND status:500
```

## Lab Exercise

Point your homelab's syslog output (firewall, servers) at Graylog, build a simple dashboard showing failed-login counts, and set an alert rule for a spike over a threshold.

## Related Tools

- [Elastic Stack / Elastic Security](elastic-stack.md) — heavier, more feature-rich alternative
