# dnsx

Fast, multi-purpose DNS toolkit for bulk resolution — part of the ProjectDiscovery pipeline, built for speed at scale.

**Links:** [GitHub](https://github.com/projectdiscovery/dnsx)

## Overview

dnsx resolves large lists of hostnames quickly and can retrieve specific record types (A, CNAME, MX, TXT, etc.), wildcard-filter results, and integrate with the same tool chain as Subfinder/httpx/Nuclei.

## Install / Deploy

```bash
go install -v github.com/projectdiscovery/dnsx/cmd/dnsx@latest
```

## Common Commands

```bash
cat subs.txt | dnsx -a -resp
cat subs.txt | dnsx -cname -resp
dnsx -l subs.txt -wd example.com   # wildcard filtering
```

## Lab Exercise

Pipe [Subfinder](subfinder.md) output into dnsx to resolve which subdomains actually have DNS records before feeding the live list to [httpx](httpx.md).

## Related Tools

- [Subfinder](subfinder.md) · [httpx](httpx.md) — pipeline neighbors
