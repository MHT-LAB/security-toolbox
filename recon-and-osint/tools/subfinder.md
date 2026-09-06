# Subfinder

Fast passive subdomain discovery from ProjectDiscovery — queries dozens of OSINT sources in parallel and returns clean, deduplicated results.

**Links:** [GitHub](https://github.com/projectdiscovery/subfinder) · [Docs](https://docs.projectdiscovery.io/tools/subfinder)

## Overview

Subfinder is built for speed and pipeline use — it's the tool most ProjectDiscovery workflows (`subfinder | httpx | nuclei`) start with. Passive-only by default, so it doesn't touch the target directly.

## Install / Deploy

```bash
go install -v github.com/projectdiscovery/subfinder/v2/cmd/subfinder@latest
```

## Common Commands

```bash
subfinder -d example.com
subfinder -d example.com -all -o subs.txt   # use all sources, save output
subfinder -dL domains.txt -o subs.txt        # bulk mode
```

## Lab Exercise

Chain Subfinder into [httpx](httpx.md) and [Nuclei](nuclei.md): `subfinder -d example.com | httpx | nuclei -t cves/` against a domain you own, to see the full ProjectDiscovery recon pipeline in one command.

## Related Tools

- [OWASP Amass](owasp-amass.md) — slower, more thorough alternative
- [httpx](httpx.md) · [Nuclei](nuclei.md) — natural next steps in the pipeline
