# Anomali ThreatStream

Commercial threat-intelligence management platform — aggregates many paid and free feeds into one enrichment/management layer.

**Links:** [Official site](https://www.anomali.com/products/threatstream) — commercial product, no public repo.

## Overview

ThreatStream's value is aggregation and management — pulling many disparate feeds (including free ones like abuse.ch and OTX) into one platform with deduplication, scoring, and integration into SIEM/SOAR tooling, rather than being a unique intel source itself.

## Install / Deploy

```text
Commercial subscription through Anomali; deployment is SaaS-hosted with
connectors configured through their admin console.
```

## Common Commands

Not applicable — commercial SaaS platform.

## Lab Exercise

If evaluating for an employer/client, compare what ThreatStream aggregates against manually configuring the same free feeds (abuse.ch, OTX, AIS) directly into [MISP](../../detect-and-respond/tools/misp.md) — the cost/benefit of aggregation-as-a-service versus DIY is the real evaluation question.

## Related Tools

- [MISP](../../detect-and-respond/tools/misp.md) — free DIY alternative for the same aggregation goal
