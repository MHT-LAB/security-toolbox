# FLARE-VM

Mandiant's Windows VM configuration for reverse engineering and malware analysis — an installer script that turns a clean Windows VM into a fully-loaded analysis environment.

**Links:** [GitHub](https://github.com/mandiant/flare-vm)

## Overview

Rather than manually installing dozens of Windows-native RE/malware-analysis tools, FLARE-VM's installer script automates the whole setup — x64dbg, PE tools, Python analysis libraries, and more, all on one VM snapshot you can revert after each analysis session.

## Install / Deploy

```powershell
# On a clean, isolated Windows VM (never your host machine):
# Download install.ps1 from the repo and run as Administrator
Set-ExecutionPolicy Unrestricted
.\install.ps1
```

## Common Commands

Not applicable — this is an environment setup, not a standalone tool; use the individual tools it installs ([x64dbg](x64dbg.md), etc.) once set up.

## Lab Exercise

Build a FLARE-VM snapshot on an isolated hypervisor VLAN, use it for the [x64dbg](x64dbg.md) lab exercise, then revert the VM to its clean snapshot afterward — this snapshot-and-revert pattern is the standard workflow for repeated malware analysis.

## Related Tools

- [x64dbg](x64dbg.md) — one of the tools it installs
- [REMnux](remnux.md) — the Linux-side equivalent environment
