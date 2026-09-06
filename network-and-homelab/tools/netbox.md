# NetBox

IPAM/DCIM tool for tracking network documentation as data, not a spreadsheet — source of truth for IP addressing, devices, racks, and cabling.

**Links:** [GitHub](https://github.com/netbox-community/netbox) · [Docs](https://netboxlabs.com/docs/netbox/)

## Overview

NetBox models your network as structured data — IP prefixes, VLANs, devices, interfaces, cable connections — instead of a spreadsheet that drifts out of date. It's also increasingly used as a "source of truth" that automation tools (Ansible) read from directly.

## Install / Deploy

```bash
git clone https://github.com/netbox-community/netbox-docker.git
cd netbox-docker && docker compose up -d
```

## Common Commands

Web-UI driven; also exposes a full REST/GraphQL API for automation.

## Lab Exercise

Document your actual homelab network in NetBox — IP prefixes, VLANs, each device and its interfaces — and see how quickly it becomes more useful than remembering which IP is which.

## Related Tools

- [LibreNMS](librenms.md) — complementary auto-discovery/monitoring, versus NetBox's manually-curated source of truth
