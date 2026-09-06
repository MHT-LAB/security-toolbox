# TrueNAS

Free NAS operating system (CORE/SCALE) — ZFS-backed storage with snapshots, replication, and a web UI for managing shares and apps.

**Links:** [GitHub](https://github.com/truenas/middleware) · [Docs](https://www.truenas.com/docs/)

## Overview

TrueNAS turns spare drives into a proper NAS with ZFS's data-integrity features (checksumming, snapshots, easy replication) — CORE is FreeBSD-based, SCALE is Linux-based with better container/app support. Either is the standard backing store for homelab backups and media.

## Install / Deploy

```text
Download the installer ISO from truenas.com and install to dedicated hardware
or a VM with passed-through disks (avoid virtualized disks for the actual storage pool).
```

## Common Commands

TrueNAS is primarily web-UI driven; the underlying shell supports standard ZFS commands:
```bash
zpool status
zfs list
zfs snapshot pool/dataset@backup-2026-01-01
```

## Lab Exercise

Set up a TrueNAS instance with a mirrored ZFS pool, configure a scheduled snapshot policy, then intentionally delete a test file and restore it from a snapshot to confirm the recovery workflow actually works.

## Related Tools

- [Proxmox VE](proxmox-ve.md) — commonly runs alongside it as the hypervisor host
