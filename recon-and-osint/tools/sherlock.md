# Sherlock

Finds usernames across social media platforms — checks a given username against hundreds of sites and reports where an account exists.

**Links:** [GitHub](https://github.com/sherlock-project/sherlock)

## Overview

Given a username, Sherlock checks it against a large, community-maintained list of sites and reports hits — useful for building a picture of someone's public footprint during authorized OSINT work (e.g. social-engineering-assessment prep).

## Install / Deploy

```bash
git clone https://github.com/sherlock-project/sherlock.git
cd sherlock && pip install -r requirements.txt
```

## Common Commands

```bash
python3 sherlock username123
python3 sherlock username123 --timeout 10 --print-found
```

## Lab Exercise

Run Sherlock against a username you own across multiple platforms, and manually verify each reported hit — false positives happen, so treat results as leads to confirm, not final facts.

## Related Tools

- [GHunt](ghunt.md) · [Holehe](holehe.md) — complementary email/account-focused OSINT
