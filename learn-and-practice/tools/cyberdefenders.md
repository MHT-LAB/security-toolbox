# CyberDefenders

Free blue-team DFIR challenges — investigate real-world-style incident scenarios (memory dumps, pcaps, log sets) rather than triaging live alerts like LetsDefend.

**Links:** [Official site](https://cyberdefenders.org) — SaaS, no public repo.

## Overview

CyberDefenders' challenges hand you actual artifacts (a memory dump, a pcap, an EVTX export) tied to a scenario and ask specific investigative questions — good practice for applying tools like [Volatility 3](../../analyze-and-investigate/tools/volatility3.md) and [Wireshark](../../analyze-and-investigate/tools/wireshark.md) to a realistic case rather than a synthetic exercise.

## Install / Deploy

```text
Free account registration at cyberdefenders.org to access the challenge archive.
```

## Common Commands

Depends on the challenge — expect to reach for [Volatility 3](../../analyze-and-investigate/tools/volatility3.md), [Wireshark](../../analyze-and-investigate/tools/wireshark.md), or [Plaso](../../analyze-and-investigate/tools/plaso.md) depending on the artifact type.

## Lab Exercise

Pick a free memory-forensics challenge, download the provided memory image, and work through it with [Volatility 3](../../analyze-and-investigate/tools/volatility3.md) exactly as you would a real incident — write up findings before checking the official write-up.

## Related Tools

- [LetsDefend](letsdefend.md) — comparable blue-team-focused alternative, live-alert style instead of artifact-based
- [Volatility 3](../../analyze-and-investigate/tools/volatility3.md) · [Wireshark](../../analyze-and-investigate/tools/wireshark.md) — frequently the tools these challenges require
