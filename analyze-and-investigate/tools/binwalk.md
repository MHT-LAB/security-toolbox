# binwalk

Firmware analysis and extraction tool — identifies and extracts embedded file systems, compressed data, and executable code from firmware images.

**Links:** [GitHub](https://github.com/ReFirmLabs/binwalk)

## Overview

binwalk scans a firmware blob for signatures of known file types/formats and can automatically extract embedded file systems (SquashFS, JFFS2, etc.), making it the standard first step in IoT/firmware security analysis.

## Install / Deploy

```bash
sudo apt install binwalk
```

## Common Commands

```bash
binwalk firmware.bin
binwalk -e firmware.bin        # extract identified components
binwalk -Me firmware.bin       # recursive extraction
```

## Lab Exercise

Download a publicly available router/IoT firmware image (from the vendor's own support site), run `binwalk -e` against it, and browse the extracted file system for configuration files or hardcoded credentials.

## Related Tools

- [FLOSS](floss.md) — complementary string extraction once you have extracted binaries
