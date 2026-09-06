# LibreNMS

Auto-discovering network monitoring platform (SNMP-based) — points at your network and maps devices/interfaces automatically rather than manual entry.

**Links:** [GitHub](https://github.com/librenms/librenms) · [Docs](https://docs.librenms.org)

## Overview

LibreNMS uses SNMP auto-discovery to find and monitor network devices (switches, routers, printers, servers) without manually adding each one — a good fit for homelab network hardware that speaks SNMP but doesn't have its own agent-based monitoring option.

## Install / Deploy

```bash
docker run -d --name librenms -p 8000:8000 \
  -e LIBRENMS_WEB_PORT=8000 librenms/librenms
```

## Common Commands

```bash
lnms device:add 10.0.0.1 -v v2c -c public
lnms discovery:run -h all
```

## Lab Exercise

Enable SNMP on a lab switch/router, add it to LibreNMS, and let auto-discovery map its interfaces — then compare the SNMP-based approach against agent-based monitoring like [Zabbix](zabbix.md) for a server you also monitor.

## Related Tools

- [Zabbix](zabbix.md) — agent-based alternative for hosts, not just network gear
- [ntopng](ntopng.md) — complementary traffic-flow visualization
