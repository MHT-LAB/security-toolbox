# Detect It Easy (DIE)

File-type and packer detection for binaries — quickly identifies what compiler/packer produced a file before you invest time in deeper reverse engineering.

**Links:** [GitHub](https://github.com/horsicq/Detect-It-Easy)

## Overview

DIE examines a binary's structure to identify its file type, compiler, and — critically for malware analysis — whether it's been packed (and by what packer), telling you whether you need to unpack it before Ghidra/radare2 analysis will be useful.

## Install / Deploy

```text
Download the release for your platform from the GitHub releases page.
```

## Common Commands

```bash
diec suspicious_file.exe          # CLI version
```

## Lab Exercise

Run DIE against a few different sample binaries (a plain compiled test program, and a UPX-packed version of the same program) to see how it distinguishes packed from unpacked files.

## Related Tools

- [Ghidra](ghidra.md) · [x64dbg](x64dbg.md) — next steps once you know what you're dealing with
