# Aquatone

Visual inventory of websites via screenshots across many hosts — turns a long list of subdomains into a browsable set of thumbnails.

**Links:** [GitHub](https://github.com/michenriksen/aquatone)

## Overview

When you have hundreds of live hosts from [httpx](httpx.md), scrolling through them one by one isn't practical — Aquatone screenshots each and builds an HTML report you can skim visually to spot login pages, admin panels, and default install pages fast.

## Install / Deploy

```bash
# Download release binary from GitHub releases page
```

## Common Commands

```bash
cat hosts.txt | aquatone
# Output: an HTML report with screenshots under ./aquatone/
```

## Lab Exercise

Feed [httpx](httpx.md)'s live-host output into Aquatone for a domain you own, and skim the resulting HTML gallery for anything that looks like an exposed admin panel or default install page worth a closer look.

## Related Tools

- [httpx](httpx.md) — typical upstream source of the host list
- [EyeWitness](eyewitness.md) — similar screenshot-gallery alternative
