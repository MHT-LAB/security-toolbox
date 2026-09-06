# Suricata

High-performance IDS/IPS and network security monitoring engine — inspects traffic against signature rules and can also extract file/protocol metadata for hunting.

**Links:** [GitHub](https://github.com/OISF/suricata) · [Docs](https://docs.suricata.io)

## Overview

Suricata reads a mirrored copy of network traffic and matches it against rulesets (community rules like ET Open, or custom Sigma-derived rules), generating alerts on known-bad patterns. It also logs rich protocol metadata (`eve.json`) useful for hunting even without a signature match.

## Install / Deploy

```bash
sudo apt install suricata
sudo suricata-update              # pull the latest ruleset
sudo suricata -i eth0 -c /etc/suricata/suricata.yaml
```

## Common Commands

```bash
suricata -T -c /etc/suricata/suricata.yaml   # test config
tail -f /var/log/suricata/fast.log           # live alert stream
jq . /var/log/suricata/eve.json | less       # browse structured events
```

## Lab Exercise

Run Suricata on a SPAN/mirror port in your homelab, then run [Nmap](../../recon-and-osint/tools/nmap.md) or [Nikto](../../test-and-exploit/tools/nikto.md) against a lab target and confirm the resulting alerts show up in `fast.log`.

## Related Tools

- [Zeek](zeek.md) — complementary protocol-analysis focus rather than signature matching
- [Security Onion](security-onion.md) — bundles Suricata with a full analysis stack
