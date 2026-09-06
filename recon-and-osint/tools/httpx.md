# httpx

Fast HTTP probing/toolkit for live-host discovery — takes a list of hosts/subdomains and reports which actually respond over HTTP(S), with metadata (status code, title, tech stack).

**Links:** [GitHub](https://github.com/projectdiscovery/httpx) · [Docs](https://docs.projectdiscovery.io/tools/httpx)

## Overview

After enumerating subdomains with [Subfinder](subfinder.md)/[OWASP Amass](owasp-amass.md), httpx is the filter step: which of those hundreds of names are actually live web services worth scanning further. It's built for piping.

## Install / Deploy

```bash
go install -v github.com/projectdiscovery/httpx/cmd/httpx@latest
```

## Common Commands

```bash
cat subs.txt | httpx -status-code -title -tech-detect
subfinder -d example.com | httpx -silent
httpx -l subs.txt -o live_hosts.txt
```

## Lab Exercise

Run the full chain `subfinder -d example.com | httpx | nuclei -t cves/` against a domain you own, and note how each tool narrows the list for the next.

## Related Tools

- [Subfinder](subfinder.md) — typical upstream source
- [Nuclei](nuclei.md) — typical downstream consumer
