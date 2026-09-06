# Cutter

GUI front end for radare2/Rizin — much friendlier for daily reverse-engineering work than raw `r2` commands, with a decompiler plugin available.

**Links:** [GitHub](https://github.com/rizinorg/cutter) · [Docs](https://cutter.re/docs/)

## Overview

Cutter gives radare2/Rizin's analysis engine a visual interface — function graphs, a hex view, and (with the Ghidra decompiler plugin installed) pseudo-C output, without needing to memorize r2's command syntax.

## Install / Deploy

```text
Download the AppImage/installer from cutter.re
```

## Common Commands

Cutter is GUI-driven; open a binary, let auto-analysis run, browse the function list and graph view.

## Lab Exercise

Open the same CTF reversing binary used in the [radare2](radare2.md) exercise in Cutter instead, and compare how much faster you can navigate the function graph visually versus the raw CLI.

## Related Tools

- [radare2](radare2.md) — the underlying engine
- [Ghidra](ghidra.md) — alternative decompiler-first tool
