# Ghidra

NSA's free software reverse-engineering suite — disassembler and decompiler covering a huge range of processor architectures, with a scripting API.

**Links:** [GitHub](https://github.com/NationalSecurityAgency/ghidra) · [Docs](https://ghidra-sre.org)

## Overview

Ghidra decompiles binaries into readable pseudo-C, letting you understand what a piece of malware or firmware actually does at the logic level rather than raw assembly — its decompiler is genuinely competitive with commercial tools like IDA Pro, at no cost.

## Install / Deploy

```text
Download the release from ghidra-sre.org (requires a JDK 17+ installed), extract, and run ghidraRun.
```

## Common Commands

Ghidra is GUI-driven: create a project, import a binary, let auto-analysis run, then browse the decompiled function listing. Its scripting console supports Python/Java for automation.

## Lab Exercise

Load a captured malware sample (from a lab-only, isolated analysis VM) or a benign CTF reversing challenge binary into Ghidra, run auto-analysis, and walk through the decompiled `main` function to understand the program's logic.

## Related Tools

- [radare2](radare2.md) · [Cutter](cutter.md) — CLI/lighter-weight alternatives
- [x64dbg](x64dbg.md) — dynamic debugging complement to Ghidra's static analysis
