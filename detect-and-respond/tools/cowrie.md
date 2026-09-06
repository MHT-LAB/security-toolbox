# Cowrie

SSH/Telnet honeypot that logs full attacker sessions, including credentials tried and commands run.

**Links:** [GitHub](https://github.com/cowrie/cowrie) · [Docs](https://cowrie.readthedocs.io)

## Overview

Cowrie emulates an SSH/Telnet server with a fake filesystem, logging every credential attempted and every command an attacker types once "in" — genuinely useful for understanding what automated SSH-scanning bots actually try to do once they think they have access.

## Install / Deploy

```bash
git clone https://github.com/cowrie/cowrie.git
cd cowrie
python3 -m venv cowrie-env && source cowrie-env/bin/activate
pip install -r requirements.txt
bin/cowrie start
```

## Common Commands

```bash
bin/cowrie start
tail -f var/log/cowrie/cowrie.json
```

## Lab Exercise

Deploy Cowrie on a lab VM's SSH port (moving the real SSH to a non-standard port first), and after exposing it briefly to the internet (isolated segment only), review the JSON log for captured credentials and commands.

## Related Tools

- [T-Pot](t-pot.md) — bundles Cowrie alongside many other honeypots
