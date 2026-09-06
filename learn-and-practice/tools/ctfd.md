# CTFd

The standard open-source platform for hosting your own CTF — challenge management, scoring, and a leaderboard, self-hosted.

**Links:** [GitHub](https://github.com/CTFd/CTFd) · [Docs](https://docs.ctfd.io)

## Overview

CTFd is what most self-hosted/private CTF events actually run on — define challenges (with flags, hints, and point values), open registration, and CTFd handles submission, scoring, and the leaderboard automatically.

## Install / Deploy

```bash
git clone https://github.com/CTFd/CTFd.git
cd CTFd && docker compose up -d
```

## Common Commands

Web-UI driven admin panel for creating challenges; a CLI (`CTFd import`/`export`) exists for bulk challenge management.

## Lab Exercise

Stand up CTFd and build a small internal CTF using challenges you create from tools already in this repo (e.g. a [CyberChef](../../analyze-and-investigate/tools/cyberchef.md) decoding puzzle, a [Juice Shop](../../test-and-exploit/tools/juice-shop.md) flag) — a good way to consolidate what you've learned by teaching it to someone else.

## Related Tools

- [rCTF](rctf.md) — lighter-weight alternative platform
