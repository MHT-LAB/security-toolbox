# Osmedeus

Automated recon pipeline/framework for continuous attack-surface monitoring — chains subdomain discovery, port scanning, and vulnerability scanning into one workflow that can run on a schedule.

**Links:** [GitHub](https://github.com/j3ssie/osmedeus)

## Overview

Rather than running each recon tool by hand, Osmedeus defines workflows (YAML) that chain them — subdomain enumeration → live-host probing → vulnerability scanning — and can be scheduled to re-run periodically, flagging what's changed since the last run.

## Install / Deploy

```bash
git clone https://github.com/j3ssie/osmedeus.git
cd osmedeus && make install
```

## Common Commands

```bash
osmedeus scan -t example.com
osmedeus scan -T targets.txt -w general
```

## Lab Exercise

Run Osmedeus's general workflow against a domain you own on a schedule (e.g. weekly), and review the diff report between runs — this is the pattern for continuous external-attack-surface monitoring rather than one-off assessments.

## Related Tools

- [Subfinder](subfinder.md) · [httpx](httpx.md) · [Nuclei](nuclei.md) — the individual tools Osmedeus chains together
