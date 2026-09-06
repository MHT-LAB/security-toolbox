# assetfinder

Finds related domains and subdomains — another single-purpose tool from tomnomnom's suite, built for fast pipeline use.

**Links:** [GitHub](https://github.com/tomnomnom/assetfinder)

## Overview

assetfinder queries a handful of sources to find subdomains and related domains, optimized for speed and piping into other tools rather than a rich standalone report.

## Install / Deploy

```bash
go install github.com/tomnomnom/assetfinder@latest
```

## Common Commands

```bash
assetfinder example.com
assetfinder --subs-only example.com | httpx
```

## Lab Exercise

Chain `assetfinder --subs-only example.com | httpx | nuclei -t cves/` against a domain you own as a lightweight alternative to the Subfinder-based pipeline.

## Related Tools

- [Subfinder](subfinder.md) · [httpx](httpx.md) — pipeline neighbors
