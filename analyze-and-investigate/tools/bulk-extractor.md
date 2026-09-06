# Bulk Extractor

Scans disk images/files for emails, URLs, and other artifacts without parsing the file system — fast, works even on damaged or partial images.

**Links:** [GitHub](https://github.com/simsong/bulk_extractor)

## Overview

Rather than requiring a valid file system structure, Bulk Extractor scans raw bytes for recognizable patterns (emails, URLs, credit card numbers, EXIF data) — useful on corrupted images or when you just need a fast first pass without full forensic parsing.

## Install / Deploy

```bash
sudo apt install bulk-extractor
```

## Common Commands

```bash
bulk_extractor -o output_dir disk.img
cat output_dir/email.txt
```

## Lab Exercise

Run Bulk Extractor against a lab disk image and review the `email.txt` and `url.txt` outputs — compare how much it finds versus a full [Autopsy](autopsy.md) ingest on the same image, and note the speed difference.

## Related Tools

- [Autopsy](autopsy.md) — fuller but slower alternative
