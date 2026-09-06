# Plaso / log2timeline

Builds super-timelines from forensic artifacts across a whole system — pulls timestamps from dozens of artifact types (registry, browser history, logs, file system) into one chronological view.

**Links:** [GitHub](https://github.com/log2timeline/plaso) · [Docs](https://plaso.readthedocs.io)

## Overview

Instead of manually correlating timestamps from the registry, browser history, event logs, and file system separately, Plaso's `log2timeline.py` parses them all and produces one combined timeline — [Timesketch](timesketch.md) then gives you a collaborative UI for reviewing it.

## Install / Deploy

```bash
pip install plaso
```

## Common Commands

```bash
log2timeline.py timeline.plaso /path/to/disk_image_or_directory
psort.py -o l2tcsv -w timeline.csv timeline.plaso
```

## Lab Exercise

Run `log2timeline.py` against a lab disk image or a directory of exported Windows event logs, export to CSV with `psort.py`, and find the exact sequence of events around a specific action (e.g. a file download followed by execution).

## Related Tools

- [Timesketch](timesketch.md) — collaborative UI for reviewing Plaso timelines
- [The Sleuth Kit](sleuthkit.md) — narrower, file-system-only timeline source
