# SpiderFoot

Automates OSINT collection across 200+ data sources, correlating results into one dashboard — the closest thing on this list to "point at a target and get a full profile back."

**Links:** [GitHub](https://github.com/smicallef/spiderfoot) · [Docs](https://www.spiderfoot.net/documentation/)

## Overview

SpiderFoot runs as a web application: give it a domain, IP, email, or name, pick which of its 200+ modules to run, and it correlates results (subdomains, leaked credentials, exposed services, social profiles) into a browsable graph.

## Install / Deploy

```bash
docker run -p 5001:5001 spiderfoot/spiderfoot
# Browse to http://localhost:5001
```

## Common Commands

SpiderFoot is primarily web-UI driven, but has a CLI mode too:
```bash
sf.py -s example.com -m sfp_dnsresolve,sfp_crt -o csv
```

## Lab Exercise

Run the "footprint" scan preset against a domain you own from the web UI, and use the correlation graph to trace how a single subdomain relates to other discovered assets — this correlation view is SpiderFoot's real value over single-purpose tools.

## Related Tools

- [Recon-ng](recon-ng.md) — similar concept, console-driven instead of web-UI
- [OWASP Amass](owasp-amass.md) — narrower, faster subdomain-only alternative
