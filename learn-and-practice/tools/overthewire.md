# OverTheWire Wargames

Free wargames for Linux, SSH, and security fundamentals — text-based, SSH-accessible challenge levels with no VM/VPN setup required.

**Links:** [Official site](https://overthewire.org/wargames/) — site-hosted, no central repo.

## Overview

OverTheWire's wargames (Bandit, Natas, Narnia, and others) are pure SSH-accessible challenge servers — no target VM to spin up, just `ssh` into the next level once you've found the previous level's password. Bandit specifically is the standard "learn the Linux command line for security" starting point.

## Install / Deploy

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

## Common Commands

Standard Linux commands (`ls`, `find`, `grep`, `cat`) — the challenge is figuring out which ones to use, not learning new tooling.

## Lab Exercise

Start with the Bandit wargame from level 0 and work through as many levels as you can without hints — it's specifically designed to build the command-line fluency every other tool in this repo assumes you already have.

## Related Tools

- [picoCTF](picoctf.md) — broader beginner-friendly CTF covering more than just Linux fundamentals
