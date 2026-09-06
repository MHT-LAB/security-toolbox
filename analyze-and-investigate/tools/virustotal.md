# VirusTotal

Free multi-engine file/URL/hash reputation lookup — checks a sample or URL against dozens of AV engines and sandboxes at once.

**Links:** [Official site](https://www.virustotal.com) — SaaS, no public core repo.

## Overview

VirusTotal aggregates detection results from dozens of AV engines plus its own sandboxing/relationship data (related samples, contacted domains, dropped files) — usually the fastest first check on any suspicious file or URL, but not a substitute for deeper analysis on genuinely novel threats.

## Install / Deploy

```bash
pip install vt-py   # official Python client
```

## Common Commands

```python
import vt
client = vt.Client("API_KEY")
file_info = client.get_object("/files/<sha256>")
```

## Lab Exercise

Check a hash or URL before you ever run it, and pivot from a VT relationship graph to find related samples/infrastructure. **Never upload sensitive or client-confidential files** — VT results are shared with its partner engines, so anything uploaded should be treated as effectively public.

## Related Tools

- [JoeSandbox](joesandbox.md) · [Hybrid Analysis](hybrid-analysis.md) — deeper sandbox alternatives
- [MISP](../../detect-and-respond/tools/misp.md) — good place to store confirmed findings
