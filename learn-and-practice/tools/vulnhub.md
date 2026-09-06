# VulnHub

Free downloadable vulnerable VMs for practice — an archive of community-built intentionally-vulnerable machines you download and run locally, no VPN/account needed.

**Links:** [Official site](https://www.vulnhub.com) — archive site, no active repo.

## Overview

VulnHub predates Hack The Box's hosted-lab model — you download a VM image (OVA/VMDK) and run it yourself in Proxmox/VirtualBox, meaning it works fully offline once downloaded and never requires a subscription.

## Install / Deploy

```text
Download a VM (e.g. one of the popular "boot2root" series) from vulnhub.com,
import it into Proxmox/VirtualBox on an isolated host-only network.
```

## Common Commands

Not applicable — the VM is the target; use [Nmap](../../recon-and-osint/tools/nmap.md)/[Metasploit](../../test-and-exploit/tools/metasploit.md)/etc. against it.

## Lab Exercise

Download a well-known beginner-rated VulnHub VM, import it on an isolated internal network alongside [Metasploitable3](../../test-and-exploit/tools/metasploitable3.md), and work it start to finish without a walkthrough before checking one against your approach.

## Related Tools

- [Metasploitable3](../../test-and-exploit/tools/metasploitable3.md) — comparable purpose-built target
