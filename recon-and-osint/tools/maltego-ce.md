# Maltego Community Edition

Link-analysis tool for mapping entity relationships (people, domains, infrastructure, social accounts) as an interactive graph.

**Links:** [Official site / CE download](https://www.maltego.com/community-edition/) — commercial product, free CE tier, no public core repository.

## Overview

Maltego's value is visual: "transforms" pull data from a source (WHOIS, DNS, social media, breach databases) and Maltego draws the resulting relationships as a graph you can keep expanding node by node. CE is rate-limited compared to paid tiers but covers most OSINT-mapping use cases.

## Install / Deploy

```text
Download the Community Edition installer from maltego.com/community-edition
(requires free registration); run the desktop client and log in.
```

## Common Commands

Maltego is graph/GUI-driven, not CLI:
- Start with a seed entity (domain, person, IP)
- Right-click → run a transform (e.g. "To DNS Name")
- Expand nodes iteratively to build the relationship graph

## Lab Exercise

Seed a graph with a domain you own, run DNS and WHOIS transforms, and expand outward until you can see the full picture of related infrastructure — then compare what the graph surfaced against a manual [OWASP Amass](owasp-amass.md) run on the same domain.

## Related Tools

- [OWASP Amass](owasp-amass.md) · [SpiderFoot](spiderfoot.md) — CLI-driven alternatives covering similar ground
