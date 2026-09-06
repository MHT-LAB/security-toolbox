# rCTF

Lightweight, scalable open-source CTF platform (used by redpwn/Ubiquity) — a simpler alternative to CTFd for hosting an event.

**Links:** [GitHub](https://github.com/redpwn/rctf)

## Overview

rCTF trades some of CTFd's plugin ecosystem for a simpler, more scalable core, favored by teams running large public CTF competitions where raw performance under load matters more than customization.

## Install / Deploy

```bash
git clone https://github.com/redpwn/rctf.git
cd rctf && docker compose up -d
```

## Common Commands

Web-UI driven; challenges are defined via config files/admin panel.

## Lab Exercise

If you've already built a small event in [CTFd](ctfd.md), rebuild the same set of challenges in rCTF and compare setup complexity and performance for the same challenge set.

## Related Tools

- [CTFd](ctfd.md) — more feature-rich alternative
