# OWASP Amass

Attack surface mapping and subdomain enumeration — combines passive OSINT sources, active DNS resolution, and scraping into one asset-discovery pipeline.

**Links:** [GitHub](https://github.com/owasp-amass/amass) · [Docs](https://github.com/owasp-amass/amass/wiki)

## Overview

Amass builds a full picture of an organization's external footprint: subdomains, associated ASNs/netblocks, and how assets relate to each other. It's heavier and more thorough than a single-purpose tool like Sublist3r, at the cost of being slower to run.

## Install / Deploy

```bash
sudo apt install amass
# or: go install -v github.com/owasp-amass/amass/v4/...@master
```

## Common Commands

```bash
amass enum -d example.com                       # passive + active enumeration
amass enum -passive -d example.com               # OSINT sources only, no active DNS
amass intel -org "Example Corp"                  # discover related domains by org name
```

## Lab Exercise

Run `amass enum -passive -d` against a domain you own or control, then cross-check the subdomain list against [Subfinder](subfinder.md)'s output on the same domain to see how much overlap/difference the two tools produce.

## Related Tools

- [Subfinder](subfinder.md) — faster, more narrowly-scoped alternative
- [httpx](httpx.md) — probe the subdomains Amass finds for live HTTP services
