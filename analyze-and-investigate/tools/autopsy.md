# Autopsy

Free digital forensics platform (GUI for The Sleuth Kit) — case management, timeline analysis, and artifact extraction from disk images in one interface.

**Links:** [GitHub](https://github.com/sleuthkit/autopsy) · [Docs](https://sleuthkit.org/autopsy/docs/)

## Overview

Autopsy wraps The Sleuth Kit's command-line forensic capabilities in a case-oriented GUI — ingest a disk image, and it automatically extracts file listings, deleted files, web history, and more into a browsable, taggable case.

## Install / Deploy

```text
Download the installer for your platform from sleuthkit.org/autopsy
(Windows-native; on Linux, build from source or use The Sleuth Kit CLI directly).
```

## Common Commands

Autopsy is GUI-driven: create a case, add a data source (disk image/logical files), let the ingest modules run, then browse results by category (Web History, Deleted Files, Keyword Hits, etc.).

## Lab Exercise

Take a disk image from a lab VM (verify its hash before and after), create an Autopsy case, and use the timeline view to reconstruct what happened around a specific event (e.g. a file being created or a program being run).

## Related Tools

- [The Sleuth Kit](sleuthkit.md) — the underlying CLI library Autopsy is built on
- [Plaso / log2timeline](plaso.md) — complementary timeline-building tool
