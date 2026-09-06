# Sigma

Generic, vendor-agnostic detection-rule format — write a detection once, convert it to your SIEM's native query language.

**Links:** [GitHub](https://github.com/SigmaHQ/sigma) · [Docs](https://sigmahq.io/docs/)

## Overview

Sigma rules describe a detection logic in YAML independent of any specific platform; converters (like [Uncoder IO](../../threat-intel-and-reference/tools/uncoder-io.md) or `sigma-cli`) translate them into Elastic, Splunk, Wazuh, or other query languages. SigmaHQ's repo ships thousands of community rules ready to convert and deploy.

## Install / Deploy

```bash
pip install sigma-cli
sigma plugin install elasticsearch
```

## Common Commands

```bash
sigma convert -t elasticsearch -p ecs_windows rule.yml
sigma convert -t splunk rule.yml
```

## Lab Exercise

Pick a Sigma rule from the SigmaHQ repo for a technique you can safely reproduce (e.g. suspicious PowerShell execution), convert it to your SIEM's query language, deploy it, and confirm it fires against the real activity.

## Related Tools

- [Uncoder IO](../../threat-intel-and-reference/tools/uncoder-io.md) — browser-based Sigma converter
- [Zircolite](zircolite.md) — runs Sigma rules directly against EVTX without a SIEM
