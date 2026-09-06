# Chainsaw

Rapid triage/hunting over Windows event logs using Sigma rules — a fast, standalone alternative to standing up a full SIEM for EVTX analysis.

**Links:** [GitHub](https://github.com/WithSecureLabs/chainsaw) · [Docs](https://github.com/WithSecureLabs/chainsaw/wiki)

## Overview

Chainsaw applies Sigma detection rules directly against a folder of EVTX files, surfacing matches in a readable table — a fast way to triage a compromised host's event logs without needing a running SIEM.

## Install / Deploy

```text
Download the release binary from the GitHub releases page.
```

## Common Commands

```bash
chainsaw hunt evtx_folder/ -s sigma_rules/ --mapping mapping_files/sigma-mapping.yml
chainsaw search "mimikatz" evtx_folder/
```

## Lab Exercise

Export EVTX logs from a lab Windows VM after running [Mimikatz](../../test-and-exploit/tools/mimikatz.md), then run Chainsaw with a Sigma ruleset against them and confirm the relevant detection fires — compare against [Zircolite](../../detect-and-respond/tools/zircolite.md) on the same data.

## Related Tools

- [Zircolite](../../detect-and-respond/tools/zircolite.md) — similar Sigma-against-EVTX tool
- [Hayabusa](hayabusa.md) — another fast EVTX triage alternative
