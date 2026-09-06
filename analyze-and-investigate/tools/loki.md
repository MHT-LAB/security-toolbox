# Loki

Simple IOC and YARA scanner for compromise indicators — a lightweight sweep tool for checking a host against known-bad hashes, filenames, and YARA rules.

**Links:** [GitHub](https://github.com/Neo23x0/Loki)

## Overview

Loki scans a filesystem for indicators of compromise — YARA rule matches, known-bad file hashes, suspicious filenames/paths — producing a quick "is this host compromised" answer without a full forensic investigation.

## Install / Deploy

```bash
git clone https://github.com/Neo23x0/Loki.git
cd Loki && pip install -r requirements.txt
python3 loki-upgrade.py    # pull latest signature updates
```

## Common Commands

```bash
python3 loki.py -p /path/to/scan
python3 loki.py --allhds     # scan all local hard drives
```

## Lab Exercise

Run Loki against a lab VM after planting a known-bad test file (e.g. the EICAR test string, or a sample from [MalwareBazaar](../../threat-intel-and-reference/tools/abusech.md)), and confirm it correctly flags it.

## Related Tools

- [Fenrir](fenrir.md) — dependency-free bash equivalent for *nix hosts
- [YARA](yara.md) — the rule engine Loki uses internally
