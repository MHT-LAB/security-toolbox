# Shodan

Search engine for internet-connected devices — indexes banners from scanning the entire IPv4 space so you can query "what's exposed" without scanning it yourself.

**Links:** [Official site](https://www.shodan.io) · [Python CLI](https://github.com/achillean/shodan-python) — SaaS, free tier covers most lookups.

## Overview

Shodan continuously scans the internet and indexes service banners, letting you search by product, version, port, or organization. Because you're querying Shodan's index rather than scanning the target yourself, lookups are passive — no traffic touches the target's network.

## Install / Deploy

```bash
pip install shodan
shodan init <YOUR_API_KEY>
```

## Common Commands

```bash
shodan search "apache" country:US
shodan host 1.2.3.4
shodan search "org:\"Example Corp\""
```

## Lab Exercise

Query your own organization's public IP ranges periodically (`shodan search net:x.x.x.x/24`) to see what's exposed from the outside — this is the single easiest continuous-monitoring habit in this whole folder, since it requires no infrastructure of your own.

## Related Tools

- [AbuseIPDB](abuseipdb.md) — reputation lookup on anything suspicious Shodan surfaces
- [Amass](owasp-amass.md) — find the assets to search for in the first place
