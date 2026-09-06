# OpenCanary

Thinkst's free, lightweight honeypot daemon that emulates common services (SSH, RDP, SMB, HTTP, and more) and alerts on any interaction.

**Links:** [GitHub](https://github.com/thinkst/opencanary) · [Docs](https://opencanary.readthedocs.io)

## Overview

OpenCanary runs fake versions of common services on a host that should never receive legitimate traffic — any connection attempt at all is a genuine finding. It's the free, software-only counterpart to Thinkst's commercial Canary appliance.

## Install / Deploy

```bash
pip install opencanary
opencanaryd --copyconfig
opencanaryd --start
```

## Common Commands

```bash
opencanaryd --start
tail -f /var/tmp/opencanary.log
```

## Lab Exercise

Run OpenCanary on a spare lab VM with a hostname resembling a real server, enable the SSH and SMB modules, then connect to it from another lab VM and confirm an alert fires — feed that alert into [Wazuh](wazuh.md) or [TheHive](thehive.md).

## Related Tools

- [Canarytokens](canarytokens.md) — lighter-weight tripwire alternative
- [T-Pot](t-pot.md) — bundles many more honeypot services
