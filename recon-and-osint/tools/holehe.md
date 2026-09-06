# Holehe

Checks whether an email is registered on other sites — queries password-reset/registration flows across dozens of services to see which ones recognize the address.

**Links:** [GitHub](https://github.com/megadose/holehe)

## Overview

Holehe abuses the "forgot password"/signup response differences most sites have (does it say "email sent" vs "no account found") to determine which platforms an email is registered on, without ever logging in.

## Install / Deploy

```bash
pip install holehe
```

## Common Commands

```bash
holehe target@example.com
holehe target@example.com --only-used   # show only positive hits
```

## Lab Exercise

Run Holehe against an email address you own that you know is registered on several services, and confirm the tool correctly identifies them — a good sanity check before trusting its output on a real assessment.

## Related Tools

- [Sherlock](sherlock.md) · [GHunt](ghunt.md) — complementary identity OSINT
