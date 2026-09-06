# Fenrir

Bash-based IOC scanner for *nix hosts, no dependencies to install — Loki's simpler sibling for Linux/Unix systems.

**Links:** [GitHub](https://github.com/Neo23x0/Fenrir)

## Overview

Fenrir is a single bash script (no Python, no dependencies) that checks a *nix filesystem against IOC lists — hashes, filenames, C2 strings — making it useful for quick triage on a host where installing anything extra isn't practical or desirable.

## Install / Deploy

```bash
git clone https://github.com/Neo23x0/Fenrir.git
chmod +x fenrir.sh
```

## Common Commands

```bash
./fenrir.sh /path/to/scan
./fenrir.sh -c hashes.txt /path/to/scan   # custom hash IOC list
```

## Lab Exercise

Run Fenrir against a lab Linux VM with a planted test IOC (a file matching a hash in a custom IOC list you create), and confirm the scan flags it — useful for understanding what a truly dependency-free triage tool looks like.

## Related Tools

- [Loki](loki.md) — Python-based equivalent with YARA support, for Windows/broader use
