# Vulnerable-AD

Scripts to build a deliberately misconfigured AD environment for practice — a simpler, single-domain alternative to GOAD's multi-domain forest.

**Links:** [GitHub](https://github.com/WazeHell/vulnerable-AD)

## Overview

Vulnerable-AD is a PowerShell script that populates a fresh AD domain with common misconfigurations (weak ACLs, Kerberoastable accounts, unconstrained delegation) — faster to stand up than GOAD when you just need one realistic vulnerable domain rather than a multi-domain forest.

## Install / Deploy

```powershell
# Run on a fresh Windows Server domain controller VM:
git clone https://github.com/WazeHell/vulnerable-AD.git
.\vulnad.ps1
```

## Common Commands

Not applicable — the script configures the domain; use [BloodHound](../../test-and-exploit/tools/bloodhound.md)/[Impacket](../../test-and-exploit/tools/impacket.md) against the result.

## Lab Exercise

Build a single-domain lab with Vulnerable-AD when you want a quicker setup than GOAD, run a [BloodHound](../../test-and-exploit/tools/bloodhound.md) collector, and confirm the same attack-path concepts apply at smaller scale.

## Related Tools

- [GOAD](goad.md) — heavier, multi-domain alternative
