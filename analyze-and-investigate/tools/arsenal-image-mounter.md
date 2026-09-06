# Arsenal Image Mounter

Mounts forensic disk images as drives on Windows for native tool access — lets Windows Explorer, antivirus scanners, or any native tool treat a forensic image like a real attached disk.

**Links:** [GitHub](https://github.com/ArsenalRecon/Arsenal-Image-Mounter)

## Overview

Rather than extracting files from an image with a forensic tool one at a time, Arsenal Image Mounter mounts the entire image (read-only) as a virtual disk, letting you browse it in Explorer or run any Windows-native tool against it directly.

## Install / Deploy

```text
Download and install from the GitHub releases page (Windows only).
```

## Common Commands

GUI-driven: Mount → select image file → choose read-only mount mode → browse the resulting drive letter.

## Lab Exercise

Mount a lab disk image read-only with Arsenal Image Mounter, then run a quick antivirus scan or manual browse of the mounted drive to spot-check for obvious artifacts before deeper analysis in [Autopsy](autopsy.md).

## Related Tools

- [Autopsy](autopsy.md) — deeper structured analysis of the same image
