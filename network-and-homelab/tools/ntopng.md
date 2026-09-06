# ntopng

Real-time network traffic monitoring and visualization — see live bandwidth usage by host, application, and protocol.

**Links:** [GitHub](https://github.com/ntop/ntopng) · [Docs](https://www.ntop.org/guides/ntopng/)

## Overview

ntopng gives a real-time, visual view of "who's using the bandwidth right now" — useful for spotting an unexpected high-traffic host or application on a homelab network without digging through raw NetFlow data by hand.

## Install / Deploy

```bash
sudo apt install ntopng
sudo systemctl start ntopng
```

## Common Commands

Web-UI driven at `http://localhost:3000`; no CLI needed for basic monitoring.

## Lab Exercise

Run ntopng on your homelab router/gateway (or fed by a SPAN port), generate some traffic (e.g. a file transfer), and confirm it shows up correctly attributed by host and application in the live dashboard.

## Related Tools

- [nfdump](../../detect-and-respond/tools/nfdump.md) — complementary NetFlow-based analysis for longer retention
