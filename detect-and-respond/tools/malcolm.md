# Malcolm

Zeek/Suricata/Arkime bundle from Idaho National Lab, container-deployed — another integrated NSM stack, aimed at easy Docker-based deployment.

**Links:** [GitHub](https://github.com/idaholab/Malcolm)

## Overview

Malcolm packages Zeek, Suricata, and Arkime (plus an OpenSearch dashboard) as a Docker Compose stack, aimed at fast deployment (including air-gapped/offline install support) — notably used in ICS/OT security contexts given its INL origin.

## Install / Deploy

```bash
git clone https://github.com/idaholab/Malcolm.git
cd Malcolm && ./scripts/install.py
docker-compose up -d
```

## Common Commands

Deployment/config via the bundled `install.py` and `auth_setup` scripts; day-to-day use is through the OpenSearch Dashboards web UI.

## Lab Exercise

Deploy Malcolm against a SPAN port in your lab, feed it some traffic, and use the Arkime-derived session-search view to pull the pcap for a specific connection — compare against a native [Arkime](arkime.md) deployment for the same task.

## Related Tools

- [Arkime](arkime.md) — one of the components Malcolm bundles
- [Conpot](conpot.md) (ICS honeypot) — pairs conceptually if you're in an OT-adjacent lab
