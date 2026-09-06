# GOAD (Game of Active Directory)

Vulnerable-by-design Active Directory lab for practicing AD attack paths — multiple interconnected domains with intentional misconfigurations.

**Links:** [GitHub](https://github.com/Orange-Cyberdefense/GOAD)

## Overview

GOAD builds a small multi-domain AD forest riddled with realistic misconfigurations (Kerberoastable accounts, ACL abuse paths, trust relationships) — the standard practice environment for [BloodHound](../../test-and-exploit/tools/bloodhound.md)/[Impacket](../../test-and-exploit/tools/impacket.md)-style AD attack path work referenced throughout this repo.

## Install / Deploy

```bash
git clone https://github.com/Orange-Cyberdefense/GOAD.git
cd GOAD/ansible && ./goad.sh -p virtualbox -l lab -m install
```

## Common Commands

Managed via the provided `goad.sh` script and Ansible playbooks; day-to-day interaction is via the AD attack tools it's designed to be attacked with.

## Lab Exercise

Build GOAD, run a [BloodHound](../../test-and-exploit/tools/bloodhound.md) collector against it, and walk an actual privilege-escalation path to Domain Admin using [Impacket](../../test-and-exploit/tools/impacket.md)/[NetExec](../../test-and-exploit/tools/netexec.md) — this is the environment most of the AD-focused exercises elsewhere in this repo assume.

## Related Tools

- [BloodHound](../../test-and-exploit/tools/bloodhound.md) · [Impacket](../../test-and-exploit/tools/impacket.md) · [NetExec](../../test-and-exploit/tools/netexec.md) — the tools this lab is built for
- [DetectionLab](detectionlab.md) — comparable AD lab with a logging/detection focus instead
