# LevelBlue Open Threat Exchange (OTX)

Free, crowdsourced threat-intel sharing platform (formerly AlienVault OTX) — community-submitted "pulses" of related indicators, freely queryable via API.

**Links:** [Official site](https://otx.alienvault.com)

## Overview

OTX lets anyone submit and subscribe to "pulses" — grouped sets of IOCs tied to a campaign or threat — making it one of the most accessible free threat-intel sources, with both a web UI and a straightforward REST API for automated ingestion.

## Install / Deploy

```bash
pip install OTXv2
```

## Common Commands

```python
from OTXv2 import OTXv2
otx = OTXv2("API_KEY")
otx.getall()   # pull all subscribed pulses
```

## Lab Exercise

Subscribe to a few relevant pulses in the OTX web UI, then pull them via the API into [MISP](../../detect-and-respond/tools/misp.md) as an automated feed rather than checking the web UI manually.

## Related Tools

- [MISP](../../detect-and-respond/tools/misp.md) — common ingestion target for OTX pulses
- [abuse.ch](abusech.md) — comparable free community feed
