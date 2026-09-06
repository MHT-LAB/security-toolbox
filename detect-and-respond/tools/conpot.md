# Conpot

ICS/SCADA honeypot emulating industrial protocols (Modbus, S7comm) — useful for OT-adjacent homelabs or studying industrial-protocol attack patterns.

**Links:** [GitHub](https://github.com/mushorg/conpot) · [Docs](https://conpot.readthedocs.io)

## Overview

Conpot emulates common industrial control system protocols and device profiles, letting you observe how scanners and attackers probe OT-style targets without exposing anything resembling a real control system.

## Install / Deploy

```bash
git clone https://github.com/mushorg/conpot.git
cd conpot && pip install .
conpot --template default
```

## Common Commands

```bash
conpot --template default
tail -f /var/log/conpot.log
```

## Lab Exercise

Deploy Conpot on an isolated lab segment and scan it with [Nmap](../../recon-and-osint/tools/nmap.md)'s Modbus-detection scripts to see what a legitimate OT-asset discovery scan looks like from the honeypot's side.

## Related Tools

- [T-Pot](t-pot.md) — bundles Conpot alongside many other honeypots
