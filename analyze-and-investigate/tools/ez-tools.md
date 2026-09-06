# Eric Zimmerman's Tools (EZ Tools)

The de facto standard suite for Windows DFIR artifact parsing (MFTECmd, Registry Explorer, Timeline Explorer, and many more).

**Links:** [GitHub](https://github.com/EricZimmerman) · [Docs](https://ericzimmerman.github.io)

## Overview

Eric Zimmerman's tools each parse one specific Windows artifact extremely well — MFTECmd for the Master File Table, Registry Explorer for hive browsing, Timeline Explorer for reviewing CSV timelines. Most Windows DFIR workflows use several of these together.

## Install / Deploy

```text
Download individual tools (or the full KAPE bundle) from ericzimmerman.github.io —
most are standalone .NET executables, no installation required.
```

## Common Commands

```powershell
MFTECmd.exe -f "$MFT" --csv out\
RECmd.exe --bn BatchExamples\Kroll_Batch.reb -d C:\hives --csv out\
```

## Lab Exercise

Extract the MFT from a lab disk image, run it through MFTECmd, and open the resulting CSV in Timeline Explorer to reconstruct file creation/modification activity around a specific event.

## Related Tools

- [RegRipper](regripper.md) — alternative registry-analysis approach
- [KAPE](https://ericzimmerman.github.io/KapeDocs/) — triage/collection tool built around these
