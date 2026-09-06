# MITRE ATT&CK Navigator

Browser-based technique mapping against the ATT&CK framework — visualize and annotate which adversary techniques are covered by your detections (or your lab exercises).

**Links:** [GitHub](https://github.com/mitre-attack/attack-navigator)

## Overview

Navigator renders the ATT&CK matrix as an interactive grid you can color-code and annotate — commonly used to map "which techniques does my SIEM actually detect" or "which techniques did this red-team exercise cover," against the reference framework itself (see [MITRE ATT&CK](../../threat-intel-and-reference/tools/mitre-attack.md) in threat-intel-and-reference).

## Install / Deploy

```text
Use the hosted version at mitre-attack.github.io/attack-navigator,
or self-host: git clone, then `npm install && npm run start` in the nav-app directory.
```

## Common Commands

Not applicable — browser-based; build a layer by clicking techniques and assigning colors/scores, then export/save the resulting JSON layer.

## Lab Exercise

After working through several exercises in [`test-and-exploit/`](../../test-and-exploit/README.md) (Mimikatz, Responder, BloodHound), build a Navigator layer marking which ATT&CK techniques each exercise actually exercised — a good way to see your practice coverage as a map instead of a list.

## Related Tools

- [MITRE ATT&CK](../../threat-intel-and-reference/tools/mitre-attack.md) — the underlying knowledge base this visualizes
- [Sigma](../../detect-and-respond/tools/sigma.md) — detections you can map against the same framework
