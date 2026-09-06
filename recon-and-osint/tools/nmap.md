# Nmap

The standard for network discovery and port scanning — service/version detection, OS fingerprinting, and a scripting engine (NSE) for deeper checks.

**Links:** [GitHub](https://github.com/nmap/nmap) · [Docs](https://nmap.org/book/man.html)

## Overview

Nmap answers "what's alive and what's it running" for a given IP range. Beyond basic port scanning, `-sV` grabs service/version banners, `-O` attempts OS fingerprinting, and `--script` runs NSE scripts (vuln checks, brute-force, enumeration) against whatever it finds open.

## Install / Deploy

```bash
# Kali/most distros: preinstalled or `apt install nmap`
sudo apt install nmap
```

## Common Commands

```bash
nmap -sV -sC 10.0.0.0/24          # version detection + default scripts
nmap -p- -T4 target               # all 65535 ports
nmap -O target                    # OS fingerprinting
nmap --script vuln target         # run vulnerability-detection NSE scripts
```

## Lab Exercise

Run a full `-p- -sV -sC` scan against [Metasploitable3](../../test-and-exploit/tools/metasploitable3.md), then use the output to search [Metasploit](../../test-and-exploit/tools/metasploit.md) for a matching exploit module — this is the standard recon-to-exploit handoff.

## Related Tools

- [Masscan](masscan.md) — faster first pass across large ranges before Nmap's detailed scan
- [Metasploit](../../test-and-exploit/tools/metasploit.md) — what you do with Nmap's findings
