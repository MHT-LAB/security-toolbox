# CISA Automated Indicator Sharing (AIS)

Free, real-time bidirectional machine-to-machine indicator sharing with the US government.

**Links:** [Official site](https://www.cisa.gov/ais)

## Overview

AIS lets organizations submit and receive threat indicators in STIX format over TAXII, in real time and automatically — the government-run counterpart to community feeds like abuse.ch, aimed at broad, fast indicator distribution across critical infrastructure sectors.

## Install / Deploy

```text
Register for AIS access at cisa.gov/ais (free); connect via a TAXII client
— most commonly through MISP's or OpenCTI's built-in TAXII feed connector.
```

## Common Commands

Not applicable directly — configure via your TAXII-capable platform:
```text
# In MISP: Sync Actions → Feeds → add a TAXII feed pointing at AIS's TAXII server
```

## Lab Exercise

Connect a TAXII client (through [MISP](../../detect-and-respond/tools/misp.md) or [OpenCTI](../../detect-and-respond/tools/opencti.md)) to AIS to pull STIX-formatted indicators automatically rather than reading advisories by hand.

## Related Tools

- [MISP](../../detect-and-respond/tools/misp.md) · [OpenCTI](../../detect-and-respond/tools/opencti.md) — typical TAXII client platforms
