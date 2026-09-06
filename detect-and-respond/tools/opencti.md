# OpenCTI

Open-source threat intel platform for structuring and correlating IOCs — organizes intelligence as connected entities (threat actors, campaigns, malware, indicators) rather than flat indicator lists.

**Links:** [GitHub](https://github.com/OpenCTI-Platform/opencti) · [Docs](https://docs.opencti.io)

## Overview

Where [MISP](misp.md) focuses on sharing indicators, OpenCTI focuses on the relationships between them — linking an indicator to a malware family, a campaign, and a threat actor using the STIX2 data model, with connectors that pull in feeds automatically (MITRE ATT&CK, MISP, AbuseIPDB, and more).

## Install / Deploy

```bash
git clone https://github.com/OpenCTI-Platform/docker.git
cd docker && cp .env.sample .env   # set required env vars
docker-compose up -d
```

## Common Commands

OpenCTI is primarily web-UI driven, with a GraphQL API for automation:
```bash
curl -H "Authorization: Bearer $OPENCTI_TOKEN" \
  -X POST https://opencti.local/graphql -d '{"query": "{ threatActors { edges { node { name } } } }"}'
```

## Lab Exercise

Deploy OpenCTI, enable the MITRE ATT&CK connector, and import a MISP feed, then explore how OpenCTI links a specific indicator back to a technique and threat actor — this relationship view is the whole point of the platform.

## Related Tools

- [MISP](misp.md) — common data source/connector
- [MITRE ATT&CK](../../threat-intel-and-reference/tools/mitre-attack.md) — the framework OpenCTI maps against
