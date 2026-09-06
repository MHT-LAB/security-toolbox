# GHunt

Investigates Google accounts via public data — calendar, maps reviews, YouTube activity, and other artifacts exposed by a Google account's public footprint.

**Links:** [GitHub](https://github.com/mxrch/GHunt)

## Overview

Given a Gmail address, GHunt pulls together whatever public Google-account metadata is exposed (profile photo, associated YouTube channel, public calendar, Maps reviews) — a narrow but often surprisingly revealing OSINT source.

## Install / Deploy

```bash
pip install ghunt
ghunt login   # requires authenticating with your own Google cookies
```

## Common Commands

```bash
ghunt email target@gmail.com
```

## Lab Exercise

Run GHunt against a Gmail account you own with public activity enabled, to see exactly what's exposed by default — a useful exercise for understanding what to lock down in your own account's privacy settings.

## Related Tools

- [Sherlock](sherlock.md) · [Holehe](holehe.md) — complementary username/email OSINT
