# waybackurls

Pulls historical URLs for a domain from the Wayback Machine — a narrower, single-source version of what gau covers more broadly.

**Links:** [GitHub](https://github.com/tomnomnom/waybackurls)

## Overview

Simple, single-purpose tool from tomnomnom's suite: query the Wayback Machine's CDX API for every URL it has archived under a domain. Fast, no API key needed.

## Install / Deploy

```bash
go install github.com/tomnomnom/waybackurls@latest
```

## Common Commands

```bash
echo example.com | waybackurls
cat domains.txt | waybackurls > urls.txt
```

## Lab Exercise

Run waybackurls against a domain you own and compare its output against [gau](gau.md)'s multi-source results on the same domain — useful for understanding when the extra sources actually matter.

## Related Tools

- [gau](gau.md) — broader, multi-source alternative
- [assetfinder](assetfinder.md) — related domain/subdomain discovery
