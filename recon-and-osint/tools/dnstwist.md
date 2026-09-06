# dnstwist

Detects typosquatting and phishing domains that mimic yours — generates permutations of your domain (character swaps, insertions, homoglyphs) and checks which are registered.

**Links:** [GitHub](https://github.com/elceef/dnstwist)

## Overview

dnstwist generates every plausible typo/permutation of a domain (`examp1e.com`, `example-corp.com`, `exampl.com`) and checks DNS/WHOIS to see which are registered — a defensive OSINT tool for catching phishing/brand-abuse domains targeting your own org.

## Install / Deploy

```bash
pip install dnstwist
```

## Common Commands

```bash
dnstwist example.com
dnstwist --registered example.com     # only show domains that are actually registered
dnstwist --format json example.com > results.json
```

## Lab Exercise

Run dnstwist against your own domain (or a domain you own for testing) on a recurring schedule, and diff the "registered" list run over run to catch newly-registered lookalike domains as they appear.

## Related Tools

- [AbuseIPDB](abuseipdb.md) — check reputation on any suspicious lookalike domain's hosting IP
