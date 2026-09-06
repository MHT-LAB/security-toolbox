# MISP

Open-source threat intelligence sharing platform — the standard hub for storing, correlating, and sharing indicators of compromise (IOCs) between organizations and tools.

**Links:** [GitHub](https://github.com/MISP/MISP) · [Docs](https://www.misp-project.org/documentation/)

## Overview

MISP stores indicators as structured "events" with tags, taxonomies, and correlation across your own data — and connects outward to feeds like [AIS](../../threat-intel-and-reference/tools/cisa-ais.md) and [OTX](../../threat-intel-and-reference/tools/otx.md) via TAXII/API. It's both a consumer of external threat intel and a distributor of your own findings back to partners.

## Install / Deploy

```bash
# Official docker image:
docker run -p 443:443 ghcr.io/misp/misp-docker/misp-core:latest
```

## Common Commands

MISP is primarily web-UI driven; PyMISP automates the rest:
```python
from pymisp import PyMISP
misp = PyMISP('https://misp.local', 'API_KEY', False)
misp.search(controller='events', tags='tlp:red')
```

## Lab Exercise

Deploy MISP, connect a free feed like [abuse.ch](../../threat-intel-and-reference/tools/abusech.md)'s URLhaus, and confirm indicators auto-populate — then manually create an event for a finding from your own lab (e.g. a hash from [CAPEv2](../../analyze-and-investigate/tools/capev2.md)) and tag it correctly.

## Related Tools

- [OpenCTI](opencti.md) — relationship-focused alternative/complement
- [abuse.ch](../../threat-intel-and-reference/tools/abusech.md) · [CISA AIS](../../threat-intel-and-reference/tools/cisa-ais.md) — common feed sources
