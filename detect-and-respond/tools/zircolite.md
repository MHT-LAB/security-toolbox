# Zircolite

Standalone Sigma rule matcher for EVTX/Windows event logs, no SIEM required — point it at a log export and get Sigma-rule matches back directly.

**Links:** [GitHub](https://github.com/wagga40/Zircolite)

## Overview

Zircolite runs the entire SigmaHQ ruleset against a Windows EVTX export (or a live system's logs) without needing to stand up Elastic or Splunk first — a fast way to triage a single suspicious host.

## Install / Deploy

```bash
git clone https://github.com/wagga40/Zircolite.git
cd Zircolite && pip install -r requirements.txt
```

## Common Commands

```bash
python3 zircolite.py --evtx /path/to/evtx_folder --ruleset rules/rules_windows_generic.json
python3 zircolite.py --evtx logs/ --package full   # broader ruleset package
```

## Lab Exercise

Export EVTX logs from a lab Windows VM after running a benign-but-suspicious action (e.g. PowerShell with an encoded command), run Zircolite against the export, and confirm the matching Sigma rule fires.

## Related Tools

- [Sigma](sigma.md) — the rule format Zircolite consumes
- [Chainsaw](../../analyze-and-investigate/tools/chainsaw.md) — similar EVTX triage tool
