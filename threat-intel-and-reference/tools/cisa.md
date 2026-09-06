# CISA

The umbrella site for CISA's resources: advisories, alerts, and the Known Exploited Vulnerabilities (KEV) catalog.

**Links:** [Official site](https://www.cisa.gov)

## Overview

Beyond [AIS](cisa-ais.md) and the [best-practices hub](cisa-best-practices.md), CISA's main site is the source for time-sensitive advisories and — notably — the KEV catalog, which lists vulnerabilities confirmed to be actively exploited and is increasingly used as a patching-priority reference across the industry.

## Install / Deploy

```text
No installation — browse cisa.gov/known-exploited-vulnerabilities-catalog directly,
or pull the KEV catalog as JSON/CSV for automated ingestion.
```

## Common Commands

```bash
curl -s https://www.cisa.gov/sites/default/files/feeds/known_exploited_vulnerabilities.json
```

## Lab Exercise

Pull the current KEV catalog and cross-reference it against software versions running in your homelab or [Metasploitable3](../../test-and-exploit/tools/metasploitable3.md) — anything matching is a genuinely high-priority, real-world-exploited finding, not just theoretical.

## Related Tools

- [CISA AIS](cisa-ais.md) · [CISA Cybersecurity Best Practices](cisa-best-practices.md) — the other CISA resources
- [Exploit Database](../../test-and-exploit/tools/exploit-database.md) — find a PoC for anything on the KEV list
