# dnsrecon

DNS enumeration and zone-transfer testing — checks for a classic but still-common misconfiguration (an open zone transfer) alongside standard record enumeration.

**Links:** [GitHub](https://github.com/darkoperator/dnsrecon)

## Overview

dnsrecon covers standard record enumeration, subdomain brute-forcing, reverse lookups, and specifically checks whether a domain's nameservers allow zone transfers (`AXFR`) to anyone who asks — still worth checking, since it occasionally turns up on real assessments.

## Install / Deploy

```bash
sudo apt install dnsrecon
```

## Common Commands

```bash
dnsrecon -d example.com
dnsrecon -d example.com -t axfr        # zone-transfer check
dnsrecon -d example.com -D subdomains.txt -t brt   # brute force
```

## Lab Exercise

Set up a lab BIND/Unbound zone with transfers intentionally misconfigured (allow-any), then confirm `dnsrecon -t axfr` actually catches it — a good way to understand what "properly locked down" DNS looks like from the other side.

## Related Tools

- [dnsenum](dnsenum.md) — similar classic tool, different feature emphasis
