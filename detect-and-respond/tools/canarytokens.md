# Canarytokens

Thinkst's free, self-hostable canary-token generator — makes tripwire files, URLs, AWS keys, DNS records, and more that alert the instant someone touches them.

**Links:** [GitHub](https://github.com/thinkst/canarytokens) · [Free hosted service](https://canarytokens.org)

## Overview

A canary token is a fake credential/file/link planted somewhere an attacker would look. Legitimate users never touch it, so any alert is by definition a real finding — no tuning required, unlike almost everything else in this folder.

## Install / Deploy

```text
Easiest path: generate tokens directly at canarytokens.org (free, hosted, no signup for basic use).
Self-hosted: git clone https://github.com/thinkst/canarytokens.git and follow the repo's
docker-compose setup if you want your own token server instead of the hosted one.
```

## Common Commands

Not applicable — generate a token type (AWS key, Word doc, DNS token, URL, etc.) from the web UI, download/copy it, and place it where an attacker would find it.

## Lab Exercise

Generate a fake `credentials.xlsx` canary token, drop it on a lab file share, and confirm you get an email alert the moment it's opened — then do the same with an AWS-key token dropped in a dummy git repo.

## Related Tools

- [OpenCanary](opencanary.md) — full honeypot service alongside these lightweight tripwires
