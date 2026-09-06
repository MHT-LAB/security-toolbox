# CrowdSec

Collaborative, behavior-based intrusion detection with community threat-signal sharing — parses logs for attack patterns and can automatically ban offending IPs via "bouncers."

**Links:** [GitHub](https://github.com/crowdsecurity/crowdsec) · [Docs](https://docs.crowdsec.net)

## Overview

CrowdSec parses local logs for attack behavior (like Fail2ban) but adds a crowdsourced reputation layer — IPs flagged by other CrowdSec users worldwide get blocked before they even try your service. "Bouncers" are the enforcement plugins (nginx, iptables, etc.) that act on decisions.

## Install / Deploy

```bash
curl -s https://install.crowdsec.net | sudo sh
sudo apt install crowdsec
sudo apt install crowdsec-firewall-bouncer-iptables
```

## Common Commands

```bash
sudo cscli decisions list
sudo cscli metrics
sudo cscli hub list
```

## Lab Exercise

Deploy CrowdSec on a lab-facing SSH/web service, run a small brute-force attempt against it (with [Hydra](../../test-and-exploit/tools/hydra.md)), and confirm both a local decision and the ban actually take effect via the installed bouncer.

## Related Tools

- [Fail2ban](fail2ban.md) — simpler, non-collaborative alternative
