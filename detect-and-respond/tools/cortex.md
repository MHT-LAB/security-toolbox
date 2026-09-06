# Cortex

Observable-analysis engine that pairs with TheHive for automated enrichment — runs an IP/hash/domain through configured analyzers (VirusTotal, AbuseIPDB, etc.) automatically.

**Links:** [GitHub](https://github.com/TheHive-Project/Cortex) · [Docs](https://docs.strangebee.com/cortex/)

## Overview

Rather than manually pasting an indicator into VirusTotal/AbuseIPDB/Shodan one at a time, Cortex runs configured "analyzers" against an observable automatically and returns structured results back into TheHive's case timeline.

## Install / Deploy

```bash
docker run -p 9001:9001 thehiveproject/cortex:3
# Configure analyzers (API keys for VirusTotal, AbuseIPDB, etc.) in the web UI
```

## Common Commands

Cortex is primarily driven from TheHive's UI once connected; standalone API:
```bash
curl -H "Authorization: Bearer $CORTEX_API_KEY" \
  -X POST https://cortex.local/api/analyzer/VirusTotal_GetReport/run \
  -d '{"data":"1.2.3.4","dataType":"ip"}'
```

## Lab Exercise

Connect Cortex to TheHive, configure the VirusTotal and AbuseIPDB analyzers with free-tier API keys, then add an IP observable to a test case and confirm both analyzers auto-populate their findings.

## Related Tools

- [TheHive](thehive.md) — the case-management platform Cortex enriches
- [VirusTotal](../../analyze-and-investigate/tools/virustotal.md) · [AbuseIPDB](../../recon-and-osint/tools/abuseipdb.md) — common analyzers
