# Vuls

Agentless vulnerability scanner for Linux/FreeBSD — checks installed package versions against CVE databases over SSH, no software installed on the target.

**Links:** [GitHub](https://github.com/future-architect/vuls) · [Docs](https://vuls.io/docs/en/)

## Overview

Vuls connects over SSH to a target, inventories installed packages, and cross-references them against CVE feeds (NVD, JVN, and others) — useful for tracking exposure across a fleet of servers without deploying an agent to each one.

## Install / Deploy

```bash
git clone https://github.com/future-architect/vuls.git
cd vuls && make install
vuls configtest
```

## Common Commands

```bash
vuls scan
vuls report -format-json
```

## Lab Exercise

Point Vuls at a lab server over SSH, run a scan, and review which installed packages have known CVEs — compare its findings against what [Greenbone/OpenVAS](greenbone-openvas.md) reports for the same host.

## Related Tools

- [Greenbone/OpenVAS](greenbone-openvas.md) — heavier, network-based alternative
