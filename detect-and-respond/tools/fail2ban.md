# Fail2ban

Bans IPs showing brute-force behavior in logs — the simplest homelab win in this whole list.

**Links:** [GitHub](https://github.com/fail2ban/fail2ban) · [Docs](https://github.com/fail2ban/fail2ban/wiki)

## Overview

Fail2ban watches log files (SSH, web server, mail) for repeated failure patterns and bans the offending IP via iptables/nftables after a threshold — a five-minute setup that stops the vast majority of automated brute-force noise.

## Install / Deploy

```bash
sudo apt install fail2ban
sudo cp /etc/fail2ban/jail.conf /etc/fail2ban/jail.local
sudo systemctl enable --now fail2ban
```

## Common Commands

```bash
sudo fail2ban-client status
sudo fail2ban-client status sshd
sudo fail2ban-client set sshd unbanip 1.2.3.4
```

## Lab Exercise

Enable the `sshd` jail on a lab VM, run a few failed logins from another VM, and confirm the attacking IP gets banned within the configured threshold — then check it against [CrowdSec](crowdsec.md)'s community-reputation approach for the same scenario.

## Related Tools

- [CrowdSec](crowdsec.md) — collaborative, reputation-sharing alternative
