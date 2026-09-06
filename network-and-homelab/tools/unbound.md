# Unbound

Validating, recursive, caching DNS resolver — run your own upstream resolver instead of depending on a third-party DNS provider.

**Links:** [GitHub](https://github.com/NLnetLabs/unbound) · [Docs](https://unbound.docs.nlnetlabs.nl)

## Overview

Rather than pointing your network at 8.8.8.8 or another public resolver, Unbound resolves DNS queries recursively from the root itself, with DNSSEC validation — pairs well with [Pi-hole](pi-hole.md), which handles blocking but still needs an upstream resolver to actually answer queries.

## Install / Deploy

```bash
sudo apt install unbound
```

## Common Commands

```bash
unbound-checkconf
sudo systemctl restart unbound
dig @127.0.0.1 example.com   # test resolution
```

## Lab Exercise

Configure Pi-hole to use a local Unbound instance as its upstream resolver instead of a public DNS provider, and confirm DNSSEC validation works with `dig +dnssec`.

## Related Tools

- [Pi-hole](pi-hole.md) — typically paired with Unbound as the upstream resolver
