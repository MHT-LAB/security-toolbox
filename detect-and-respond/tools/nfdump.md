# nfdump

NetFlow collection and analysis toolset — captures flow records (who talked to whom, how much data, for how long) without the storage cost of full packet capture.

**Links:** [GitHub](https://github.com/phaag/nfdump)

## Overview

NetFlow/IPFIX records are much smaller than full packets, making nfdump practical for long-term retention of "who talked to whom" data across an entire network — useful for baseline traffic analysis and retrospective investigation when full pcap isn't feasible.

## Install / Deploy

```bash
sudo apt install nfdump
# Configure a router/switch (or softflowd) to export NetFlow to nfcapd's listening port
nfcapd -w -D -l /data/flows -p 9995
```

## Common Commands

```bash
nfdump -R /data/flows -s ip/bytes -n 10   # top 10 IPs by bytes
nfdump -R /data/flows 'host 10.0.0.5'
```

## Lab Exercise

Configure a lab router/firewall (or `softflowd` on a Linux box) to export NetFlow to nfcapd, then query for top talkers over a time window — a lightweight complement to full packet capture in [Arkime](arkime.md).

## Related Tools

- [Arkime](arkime.md) — full-packet-capture alternative for when flow data isn't enough detail
- [ntopng](../../network-and-homelab/tools/ntopng.md) — real-time flow visualization
