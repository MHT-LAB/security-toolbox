# MITRE ATT&CK

The reference knowledge base of adversary tactics and techniques — the framework nearly every detection, threat-intel, and red-team tool in this repo maps against.

**Links:** [Official site](https://attack.mitre.org)

## Overview

ATT&CK catalogs real-world adversary behavior as Tactics (the "why," e.g. Persistence) and Techniques (the "how," e.g. Scheduled Task/Job) — used as the common vocabulary for describing detections, threat-actor behavior, and red-team engagement coverage across the industry. The [Navigator](../../learn-and-practice/tools/mitre-attack-navigator.md) tool visualizes it interactively.

## Install / Deploy

```text
No installation — browse attack.mitre.org directly, or download the
STIX-formatted dataset for programmatic use.
```

## Common Commands

Not applicable — a knowledge base/reference, not a tool; see [Navigator](../../learn-and-practice/tools/mitre-attack-navigator.md) for interactive use.

## Lab Exercise

Pick one technique (e.g. T1003 — OS Credential Dumping) and trace it through this repo: which tool exercises it ([Mimikatz](../../test-and-exploit/tools/mimikatz.md)), which tool could detect it ([Sysmon config](../../detect-and-respond/tools/sysmon-config.md) + [Sigma](../../detect-and-respond/tools/sigma.md)), and which lab you'd practice it in ([GOAD](../../learn-and-practice/tools/goad.md)).

## Related Tools

- [MITRE ATT&CK Navigator](../../learn-and-practice/tools/mitre-attack-navigator.md) — the interactive visualization tool
- [Sigma](../../detect-and-respond/tools/sigma.md) · [OpenCTI](../../detect-and-respond/tools/opencti.md) — commonly mapped against this framework
