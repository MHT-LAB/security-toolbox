# Stenographer

Google's full-packet-capture buffer daemon for incident triage — keeps a rolling window of raw packets so you can pull the exact traffic around an alert after the fact.

**Links:** [GitHub](https://github.com/google/stenographer)

## Overview

Stenographer isn't an analysis tool itself — it's a high-performance packet buffer that retains recent traffic on disk, indexed for fast retrieval by BPF filter, so that when an alert fires minutes or hours later, you can still pull the exact packets involved.

## Install / Deploy

```bash
git clone https://github.com/google/stenographer.git
cd stenographer && make install
sudo systemctl start stenographer
```

## Common Commands

```bash
stenoread 'host 10.0.0.5 and port 445' -o /tmp/capture.pcap
```

## Lab Exercise

Run Stenographer on your lab's SPAN port, wait a few minutes after generating some traffic, then use `stenoread` to retrieve just that traffic by filter — confirming the retrospective-capture workflow actually works before you need it during a real incident.

## Related Tools

- [Arkime](arkime.md) — similar retrospective-capture goal with built-in indexing/search UI
