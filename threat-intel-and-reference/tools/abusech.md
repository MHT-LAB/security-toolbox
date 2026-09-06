# abuse.ch

Free malware/botnet tracking feeds (MalwareBazaar, URLhaus, Feodo Tracker, ThreatFox) — some of the most widely-used free community threat feeds in existence.

**Links:** [Official site](https://abuse.ch)

## Overview

abuse.ch runs several distinct, free, high-quality feeds: MalwareBazaar (malware sample sharing), URLhaus (malicious URLs), Feodo Tracker (botnet C2 tracking), and ThreatFox (general IOC sharing) — nearly every free/open threat-intel platform (MISP, OpenCTI) has a built-in connector for these.

## Install / Deploy

```bash
# Example: query MalwareBazaar's API for a sample by hash
curl -s -X POST https://mb-api.abuse.ch/api/v1/ \
  -d "query=get_info&hash=<sha256>"
```

## Common Commands

```bash
curl -s https://urlhaus.abuse.ch/downloads/csv_recent/ | head
```

## Lab Exercise

Connect MalwareBazaar and URLhaus feeds into [MISP](../../detect-and-respond/tools/misp.md) as automated feed sources, then pull a fresh sample hash from MalwareBazaar and run it through [CAPEv2](../../analyze-and-investigate/tools/capev2.md) in your isolated analysis lab.

## Related Tools

- [MISP](../../detect-and-respond/tools/misp.md) — common ingestion target
- [CAPEv2](../../analyze-and-investigate/tools/capev2.md) — analyze samples pulled from MalwareBazaar
