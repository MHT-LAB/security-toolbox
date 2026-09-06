# Volatility 3

Memory forensics framework — parses a captured RAM image to extract running processes, network connections, injected code, and more, entirely from memory rather than disk.

**Links:** [GitHub](https://github.com/volatilityfoundation/volatility3) · [Docs](https://volatility3.readthedocs.io)

## Overview

Volatility rebuilds a picture of what was running on a system at the moment its memory was captured — process lists, DLLs loaded, network connections, and even recoverable passwords/keys still resident in RAM. It's the standard tool whenever malware analysis or incident response needs "what was actually happening" rather than what's left on disk.

## Install / Deploy

```bash
pip install volatility3
```

## Common Commands

```bash
python3 vol.py -f memory.dmp windows.pslist
python3 vol.py -f memory.dmp windows.netscan
python3 vol.py -f memory.dmp windows.malfind
```

## Lab Exercise

Capture a memory image from a lab Windows VM after running [Mimikatz](../../test-and-exploit/tools/mimikatz.md) or a Sliver implant, then use `windows.pslist` and `windows.malfind` to find evidence of the process in memory.

## Related Tools

- [Mimikatz](../../test-and-exploit/tools/mimikatz.md) · [Sliver](../../test-and-exploit/tools/sliver.md) — good things to hunt for in a memory image
