# IVRE

Network recon framework built on Nmap/Masscan/Zeek data for internal asset tracking — stores and correlates scan results in a database rather than leaving them as flat files.

**Links:** [GitHub](https://github.com/ivre/ivre)

## Overview

IVRE ingests Nmap, Masscan, and passive (Zeek) data into a searchable database, letting you track how your own network's exposed services change over time — better suited to ongoing internal asset management than one-off external recon.

## Install / Deploy

```bash
docker-compose up   # see repo's docker-compose.yml for full stack (DB + web UI)
```

## Common Commands

```bash
ivre scancli --count
ivre runscans --category network --range 10.0.0.0/24
```

## Lab Exercise

Point IVRE at your homelab subnet, run a scan, and use its web UI to query "what services are exposed" — then re-scan after a configuration change and confirm IVRE reflects the diff.

## Related Tools

- [Nmap](nmap.md) · [Masscan](masscan.md) — the scan sources IVRE ingests
- Netdata, Zabbix (see [`network-and-homelab/`](../../network-and-homelab/README.md)) — complementary ongoing-monitoring tools
