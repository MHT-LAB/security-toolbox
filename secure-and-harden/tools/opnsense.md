# OPNsense

Free, open-source firewall and router platform — the actively-forked sibling of pfSense, with a modern web UI and a faster plugin-release cadence.

**Links:** [GitHub](https://github.com/opnsense/core) · [Docs](https://docs.opnsense.org)

## Overview

OPNsense provides a full router/firewall feature set (stateful firewall, VPN, IDS/IPS via Suricata integration, traffic shaping) through a web UI, on top of FreeBSD — a common homelab and small-business edge firewall choice.

## Install / Deploy

```text
Download the installer ISO from opnsense.org and install to dedicated hardware
or a VM with at least two network interfaces (WAN/LAN).
```

## Common Commands

OPNsense is primarily web-UI driven; the underlying FreeBSD shell is available via console/SSH for advanced troubleshooting (`pfctl -sr` to list active firewall rules).

## Lab Exercise

Deploy OPNsense as your lab's edge firewall, enable its Suricata IDS plugin, and confirm it flags an [Nmap](../../recon-and-osint/tools/nmap.md) scan run against it from another lab VM.

## Related Tools

- [Suricata](../../detect-and-respond/tools/suricata.md) — the IDS engine OPNsense can run
- [pfSense](../../network-and-homelab/README.md) — the sibling project this forked from
