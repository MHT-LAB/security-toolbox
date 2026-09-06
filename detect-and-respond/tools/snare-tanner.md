# SNARE & TANNER

Modern web-application honeypot pair — SNARE serves cloned pages, TANNER drives the detection/response logic — the successor to the older Glastopf project.

**Links:** [GitHub (SNARE)](https://github.com/mushorg/snare) · [GitHub (TANNER)](https://github.com/mushorg/tanner)

## Overview

SNARE clones a real website's pages to serve as bait, while TANNER analyzes incoming requests against known attack patterns and decides how SNARE should respond — splitting "look like a real site" from "detect what's actually happening" into two cooperating components.

## Install / Deploy

```bash
git clone https://github.com/mushorg/tanner.git && cd tanner && docker-compose up -d
git clone https://github.com/mushorg/snare.git && cd snare
python3 snare.py --target-url https://example.com   # clone a page to serve as bait
```

## Common Commands

```bash
python3 snare.py --target-url https://example.com --page-count 10
docker logs tanner_tanner_1   # review TANNER's detection output
```

## Lab Exercise

Clone a simple lab-only page with SNARE, connect it to a running TANNER instance, and run [Nikto](../../test-and-exploit/tools/nikto.md) or [sqlmap](../../test-and-exploit/tools/sqlmap.md) against it to see how TANNER classifies and logs the resulting attack attempts.

## Related Tools

- [Nikto](../../test-and-exploit/tools/nikto.md) · [sqlmap](../../test-and-exploit/tools/sqlmap.md) — good test traffic generators for this honeypot
