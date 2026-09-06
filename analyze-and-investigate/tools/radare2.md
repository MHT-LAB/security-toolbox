# radare2

Command-line reverse-engineering framework — disassembler, debugger, and binary analysis toolkit, scriptable and highly extensible.

**Links:** [GitHub](https://github.com/radareorg/radare2) · [Docs](https://book.rada.re)

## Overview

radare2 is powerful but has a notoriously steep CLI learning curve — most people now use it either scripted or through [Cutter](cutter.md)'s GUI, but the underlying `r2` command line remains the reference for scriptable, automatable binary analysis.

## Install / Deploy

```bash
git clone https://github.com/radareorg/radare2.git
cd radare2 && sys/install.sh
```

## Common Commands

```bash
r2 -A binary_file        # open with auto-analysis
# inside r2:
afl                       # list functions
pdf @ main                # disassemble the main function
```

## Lab Exercise

Open a CTF reversing challenge binary with `r2 -A`, list functions with `afl`, and disassemble the entry point — then open the same binary in [Cutter](cutter.md) to compare the CLI and GUI workflows.

## Related Tools

- [Cutter](cutter.md) — GUI front end for radare2/Rizin
- [Ghidra](ghidra.md) — decompiler-focused alternative
