# Sn1per

Automated pentest recon scanner that chains many of the above tools — one command runs Nmap, Nikto, subdomain enumeration, and more, dropping everything into one report.

**Links:** [GitHub](https://github.com/1N3/Sn1per)

## Overview

Sn1per wraps a large chunk of this repo's recon tools (Nmap, Nikto, dnsrecon, and others) behind one workflow, aimed at quickly building a first-pass picture of a target without running each tool separately.

## Install / Deploy

```bash
git clone https://github.com/1N3/Sn1per.git
cd Sn1per && bash install.sh
```

## Common Commands

```bash
sniper -t target.com -m normal
sniper -t target.com -m stealth   # lighter-footprint mode
```

## Lab Exercise

Run Sn1per in normal mode against [Metasploitable3](../../test-and-exploit/tools/metasploitable3.md) and review the combined report — then spot-check a few findings by re-running the individual underlying tool (Nmap, Nikto) yourself to confirm accuracy.

## Related Tools

- [Nmap](nmap.md) · [Nikto](../../test-and-exploit/tools/nikto.md) — among the tools Sn1per chains
