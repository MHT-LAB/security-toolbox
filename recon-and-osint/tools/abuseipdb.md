# AbuseIPDB

Free crowdsourced IP-address reputation and abuse-report lookup — check whether an IP has been reported for malicious activity before you trust or block it.

**Links:** [Official site](https://www.abuseipdb.com) — SaaS, no public repo.

## Overview

AbuseIPDB aggregates community-submitted abuse reports (brute-force attempts, spam, scanning) per IP address, giving a confidence score and report history. It's a quick sanity check on any IP surfacing in recon output or alerts.

## Install / Deploy

```text
Free account registration at abuseipdb.com gets you an API key.
```

## Common Commands

```bash
curl -G https://api.abuseipdb.com/api/v2/check \
  --data-urlencode "ipAddress=1.2.3.4" \
  -H "Key: $ABUSEIPDB_API_KEY" -H "Accept: application/json"
```

## Lab Exercise

Pipe any suspicious IPs your [Responder](../../test-and-exploit/tools/responder.md) logs or honeypot ([OpenCanary](../../detect-and-respond/tools/opencanary.md)) alerts surface through the AbuseIPDB API as an automated enrichment step, rather than checking manually one at a time.

## Related Tools

- [Shodan](shodan.md) — complementary passive lookup on the same IP
