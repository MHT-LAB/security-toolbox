# Zeek

Network traffic analysis framework — pairs well with a homelab SPAN/mirror port, generating rich structured logs (connections, DNS, HTTP, files) rather than simple alerts.

**Links:** [GitHub](https://github.com/zeek/zeek) · [Docs](https://docs.zeek.org)

## Overview

Where Suricata is signature-driven, Zeek is a scripting/analysis framework that produces detailed structured logs of every protocol it understands — connection records, DNS queries, HTTP transactions, extracted files — making it the tool of choice for retrospective hunting rather than real-time alerting alone.

## Install / Deploy

```bash
sudo apt install zeek
sudo zeekctl deploy
```

## Common Commands

```bash
zeekctl status
cat conn.log | zeek-cut id.orig_h id.resp_h id.resp_p
cat dns.log | zeek-cut query
```

## Lab Exercise

Deploy Zeek on the same SPAN port as [Suricata](suricata.md), generate some DNS and HTTP traffic in your lab, and use `zeek-cut` to pull specific fields out of `conn.log`/`dns.log` — this is the core skill for hunting through Zeek data later.

## Related Tools

- [Suricata](suricata.md) — complementary signature-based alerting
- [RockNSM](rocknsm.md) · [Malcolm](malcolm.md) — distros that bundle Zeek pre-configured
