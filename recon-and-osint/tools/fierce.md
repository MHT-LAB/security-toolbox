# Fierce

DNS reconnaissance for locating non-contiguous IP space — older tool focused on finding netblocks that belong to a target but aren't obviously linked to their main domain.

**Links:** [GitHub](https://github.com/mschwager/fierce)

## Overview

Fierce specifically hunts for IP ranges an organization owns that fall outside its "obvious" address space — useful for finding forgotten or loosely-associated infrastructure during a broader footprint assessment.

## Install / Deploy

```bash
pip install fierce
```

## Common Commands

```bash
fierce --domain example.com
fierce --domain example.com --subdomains admin dev test
```

## Lab Exercise

Run Fierce against a lab domain and compare its netblock/range findings against what a WHOIS lookup on the organization's known IPs reveals independently.

## Related Tools

- [dnsrecon](dnsrecon.md) · [dnsenum](dnsenum.md) — complementary DNS enumeration
