# RockNSM

Zeek/Suricata-based network security monitoring distro — a pre-integrated alternative to Security Onion with its own deployment model.

**Links:** [GitHub](https://github.com/rocknsm/rock)

## Overview

RockNSM bundles Zeek, Suricata, and Elastic Stack behind Ansible-based deployment automation, aimed at teams that want infrastructure-as-code control over their NSM stack rather than an ISO installer.

## Install / Deploy

```bash
git clone https://github.com/rocknsm/rock.git
cd rock && ansible-playbook -i inventory site.yml
```

## Common Commands

Deployment/management runs through Ansible playbooks; day-to-day analysis is via the bundled Kibana instance.

## Lab Exercise

Deploy RockNSM via its Ansible playbooks against a lab VM with a SPAN port, and compare the deployment experience (and resulting Kibana views) against [Security Onion](security-onion.md) for the same traffic.

## Related Tools

- [Security Onion](security-onion.md) — ISO-installer alternative covering similar ground
- [Zeek](zeek.md) · [Suricata](suricata.md) — the engines it bundles
