# RegRipper

Windows registry parsing and analysis — plugin-based extraction of forensically useful registry keys (recent files, USB history, installed software, and more).

**Links:** [GitHub](https://github.com/keydet89/RegRipper3.0)

## Overview

RegRipper runs targeted plugins against extracted registry hives (SYSTEM, SOFTWARE, NTUSER.DAT) to pull out specific forensic artifacts — much faster than manually browsing a hive in a registry editor when you know what you're looking for.

## Install / Deploy

```bash
git clone https://github.com/keydet89/RegRipper3.0.git
```

## Common Commands

```bash
rip.pl -r NTUSER.DAT -p userassist
rip.pl -r SYSTEM -p usbstor
```

## Lab Exercise

Extract the SYSTEM and NTUSER.DAT hives from a lab Windows VM's disk image, run the `usbstor` and `userassist` plugins, and confirm you can reconstruct what USB devices were connected and what programs were run.

## Related Tools

- [Eric Zimmerman's Tools](ez-tools.md) — modern alternative with broader coverage
