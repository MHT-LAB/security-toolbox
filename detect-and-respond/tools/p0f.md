# p0f

Passive OS/traffic fingerprinting from packet captures — identifies a host's operating system and other characteristics purely by observing its traffic, without any active probing.

**Links:** [GitHub](https://github.com/p0f/p0f)

## Overview

p0f fingerprints OS, uptime, and network characteristics from the way a host's TCP/IP stack behaves, entirely passively — useful for asset inventory or anomaly spotting (e.g. a host claiming to be a printer that fingerprints as a full Linux server).

## Install / Deploy

```bash
sudo apt install p0f
```

## Common Commands

```bash
sudo p0f -i eth0
sudo p0f -r capture.pcap
```

## Lab Exercise

Run p0f on your homelab's SPAN port and compare its OS fingerprints for a few known devices against their actual OS, to get a feel for its accuracy and limitations.

## Related Tools

- [Zeek](zeek.md) — complementary passive traffic analysis
