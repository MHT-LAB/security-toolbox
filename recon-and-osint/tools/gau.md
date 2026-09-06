# gau (GetAllUrls)

Fetches known URLs from Wayback Machine, Common Crawl, and OTX — a quick way to see historical endpoints without crawling the live site yourself.

**Links:** [GitHub](https://github.com/lc/gau)

## Overview

gau queries archival sources for every URL they've ever seen for a domain, surfacing old parameters, forgotten endpoints, and API paths that may still be live but are no longer linked from the current site.

## Install / Deploy

```bash
go install github.com/lc/gau/v2/cmd/gau@latest
```

## Common Commands

```bash
gau example.com
gau example.com --subs   # include subdomains
echo example.com | gau | grep "\.php"
```

## Lab Exercise

Run gau against a domain you own, filter the output for anything with a query parameter (`?`), and feed those URLs into [sqlmap](../../test-and-exploit/tools/sqlmap.md)'s batch mode to check for forgotten-but-still-injectable parameters.

## Related Tools

- [waybackurls](waybackurls.md) — similar, narrower (Wayback Machine only)
- [sqlmap](../../test-and-exploit/tools/sqlmap.md) — natural next step on parameterized URLs
