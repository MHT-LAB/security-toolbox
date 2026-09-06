# x64dbg

Open-source user-mode Windows debugger — step through a running binary, set breakpoints, and inspect memory/registers live, complementing static tools like Ghidra.

**Links:** [GitHub](https://github.com/x64dbg/x64dbg) · [Docs](https://x64dbg.com)

## Overview

Where Ghidra/radare2 analyze a binary statically, x64dbg lets you actually run it under a debugger — essential for malware that only reveals its real behavior at runtime (unpacking, anti-analysis checks, decrypting strings in memory).

## Install / Deploy

```text
Download the release from x64dbg.com, extract, and run x64dbg.exe (or x32dbg.exe for 32-bit).
Use only on an isolated Windows analysis VM — this is for running live malware samples.
```

## Common Commands

x64dbg is GUI-driven: set a breakpoint (F2), step (F7/F8), and inspect the Registers/Memory/Stack panes as execution proceeds.

## Lab Exercise

On an isolated [REMnux](remnux.md)-adjacent Windows analysis VM, run a simple packed test binary under x64dbg, step through until it unpacks itself in memory, and dump the unpacked code for further static analysis in Ghidra.

## Related Tools

- [Ghidra](ghidra.md) · [radare2](radare2.md) — static-analysis complements
- [REMnux](remnux.md) — the broader analysis-VM environment this fits into
