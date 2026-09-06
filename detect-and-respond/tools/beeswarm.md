# Beeswarm

Pairs honeypots with "honeyclients" to catch credential theft in both directions — not just servers being attacked, but clients connecting to malicious servers with bait credentials.

**Links:** [GitHub](https://github.com/honeynet/beeswarm)

## Overview

Beeswarm's twist is bidirectional: honeypots offer bait credentials, and honeyclients actively use those same credentials to connect outward — so if a credential gets stolen from the honeypot and reused elsewhere, or a honeyclient connects to a server that's been compromised, both directions get detected.

## Install / Deploy

```bash
git clone https://github.com/honeynet/beeswarm.git
cd beeswarm && pip install -e .
beeswarmc  # configure server, honeypots, and honeyclients
```

## Common Commands

```bash
beeswarm_server
beeswarm_client   # honeyclient component
```

## Lab Exercise

Deploy a Beeswarm honeypot with bait FTP credentials in an isolated lab segment, and confirm the server detects when those exact credentials are used to log in from elsewhere — a good exercise in understanding credential-reuse detection.

## Related Tools

- [Canarytokens](canarytokens.md) — simpler, single-direction bait-credential concept
