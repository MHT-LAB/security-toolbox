# Sagan

High-performance log analysis engine, Snort-rule compatible — correlates log events using a rule syntax borrowed from Snort/Suricata.

**Links:** [GitHub](https://github.com/quadrantsec/sagan)

## Overview

Sagan analyzes logs (syslog, application logs) using Snort-style rules, letting teams that already maintain Suricata/Snort rulesets extend similar logic to log-based detection rather than maintaining two separate rule languages.

## Install / Deploy

```bash
git clone https://github.com/quadrantsec/sagan.git
cd sagan && ./autogen.sh && ./configure && make && sudo make install
```

## Common Commands

```bash
sagan -c /usr/local/etc/sagan.yaml
```

## Lab Exercise

Feed a lab syslog stream (e.g. SSH auth logs) into Sagan with a rule matching repeated failed logins, and confirm it correlates and alerts the same way a Snort rule would for network traffic.

## Related Tools

- [Snort](snort.md) — the rule syntax Sagan borrows
