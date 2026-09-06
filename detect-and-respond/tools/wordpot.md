# Wordpot

WordPress-specific honeypot for catching plugin/theme exploitation attempts.

**Links:** [GitHub](https://github.com/gbrindisi/wordpot)

## Overview

Wordpot emulates a WordPress site, including specific (fake) plugins and themes, logging any request that probes for known WordPress vulnerabilities — useful given how much internet-wide scanning specifically targets WordPress installations.

## Install / Deploy

```bash
git clone https://github.com/gbrindisi/wordpot.git
cd wordpot && pip install -r requirements.txt
python3 wordpot.py
```

## Common Commands

```bash
python3 wordpot.py
tail -f wordpot.log
```

## Lab Exercise

Deploy Wordpot on a lab VM and run [WhatWeb](../../recon-and-osint/tools/whatweb.md) or [Nikto](../../test-and-exploit/tools/nikto.md) against it to confirm it correctly presents as a real WordPress site, then check what gets logged.

## Related Tools

- [Nikto](../../test-and-exploit/tools/nikto.md) — a realistic scanner to test it against
