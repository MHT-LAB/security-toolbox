# The Sleuth Kit

Command-line disk/file-system forensics library underlying Autopsy — low-level tools for examining file systems directly.

**Links:** [GitHub](https://github.com/sleuthkit/sleuthkit) · [Docs](https://www.sleuthkit.org/sleuthkit/docs.php)

## Overview

The Sleuth Kit provides the actual file-system parsing (`fls`, `icat`, `mactime`) that Autopsy's GUI sits on top of — useful when you want scriptable, headless forensic analysis rather than clicking through a GUI.

## Install / Deploy

```bash
sudo apt install sleuthkit
```

## Common Commands

```bash
fls -r -m / disk.img > bodyfile.txt          # list files, build a bodyfile
mactime -b bodyfile.txt > timeline.csv        # generate a timeline
icat disk.img <inode> > recovered_file        # extract a file by inode
```

## Lab Exercise

On a lab disk image, generate a bodyfile with `fls` and build a timeline with `mactime`, then cross-reference a specific timestamp against what [Plaso](plaso.md) produces for the same image.

## Related Tools

- [Autopsy](autopsy.md) — GUI front end for this toolkit
- [Plaso / log2timeline](plaso.md) — broader multi-source timeline tool
