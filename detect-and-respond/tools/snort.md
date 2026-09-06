# Snort

The original open-source IDS/IPS, still widely deployed — signature-based network intrusion detection, the direct ancestor of much of the modern IDS ecosystem.

**Links:** [GitHub](https://github.com/snort3/snort3) · [Docs](https://docs.snort.org)

## Overview

Snort inspects network traffic against rule-based signatures, similar to Suricata but single-threaded per instance historically (Snort 3 added multi-threading). Still common in Cisco-centric environments (Snort underlies some Cisco security products) and worth knowing even where Suricata is the newer default choice.

## Install / Deploy

```bash
sudo apt install snort
```

## Common Commands

```bash
sudo snort -T -c /etc/snort/snort.conf     # test config
sudo snort -i eth0 -c /etc/snort/snort.conf -A console
```

## Lab Exercise

Run Snort on the same SPAN port as [Suricata](suricata.md) in your lab, using an equivalent ruleset, and compare alert output/format for the same generated traffic.

## Related Tools

- [Suricata](suricata.md) — modern multi-threaded alternative
