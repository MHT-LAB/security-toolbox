# Zabbix

Full-featured infrastructure monitoring, deeper than Uptime Kuma when you outgrow it — agent-based monitoring with built-in alerting, auto-discovery, and a mature templating system.

**Links:** [GitHub](https://github.com/zabbix/zabbix) · [Docs](https://www.zabbix.com/documentation/current/en/manual)

## Overview

Zabbix is an all-in-one monitoring platform predating the Prometheus/Grafana pattern — agents installed on monitored hosts report to a central server, which handles storage, alerting, and dashboards itself rather than needing separate tools stitched together.

## Install / Deploy

```bash
docker run -d --name zabbix-server -p 10051:10051 zabbix/zabbix-server-pgsql:latest
docker run -d --name zabbix-web -p 8080:8080 zabbix/zabbix-web-nginx-pgsql:latest
```

## Common Commands

Zabbix is primarily web-UI driven; agents are configured via `zabbix_agentd.conf` on each monitored host.

## Lab Exercise

Deploy a Zabbix server, install the agent on two lab hosts, apply a built-in template (e.g. "Linux by Zabbix agent"), and confirm both hosts report in with meaningful default metrics/triggers.

## Related Tools

- [LibreNMS](librenms.md) — comparable all-in-one alternative with an SNMP/network-device focus
- [Prometheus](prometheus.md) + [Grafana](grafana.md) — the more modular alternative pattern
