# Proxmox VE

Free type-1 hypervisor for running everything else in a homelab — VM and container (LXC) management with a web UI, clustering, and built-in backup.

**Links:** [Official site](https://www.proxmox.com/en/proxmox-virtual-environment/overview) — source hosted on Proxmox's own GitLab, no primary GitHub mirror.

## Overview

Proxmox VE is the base almost every homelab in this repo assumes — it runs the VMs and LXC containers that everything else (Pi-hole, TrueNAS, Wazuh, T-Pot, lab AD environments) gets deployed onto, with a web UI for management instead of raw libvirt/KVM tooling.

## Install / Deploy

```text
Download the Proxmox VE ISO from proxmox.com and install directly to dedicated
hardware (bare-metal install, not inside another OS).
```

## Common Commands

```bash
qm list                      # list VMs
qm start <vmid>
pct list                      # list LXC containers
```

## Lab Exercise

Install Proxmox on a spare machine, create a couple of isolated internal networks (vmbr1, vmbr2) for lab segmentation, and deploy your first lab VM (e.g. [Metasploitable3](../../test-and-exploit/tools/metasploitable3.md)) onto an isolated one to confirm it has no route to your main LAN.

## Related Tools

- [TrueNAS](truenas.md) — commonly run as a VM or dedicated box alongside Proxmox
- Every lab VM in [`test-and-exploit/`](../../test-and-exploit/README.md) and [`learn-and-practice/`](../../learn-and-practice/README.md) typically runs on this
