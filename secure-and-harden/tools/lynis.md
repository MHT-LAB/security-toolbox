# Lynis

Security auditing tool for Linux/Unix systems — hundreds of automated checks against system hardening, with a scored report and specific remediation suggestions.

**Links:** [GitHub](https://github.com/CISOfy/lynis) · [Docs](https://cisofy.com/documentation/lynis/)

## Overview

Lynis scans a running system for hardening gaps — outdated packages, weak SSH config, missing kernel hardening settings, world-writable files — and reports a hardening index score plus a specific, actionable suggestion list.

## Install / Deploy

```bash
sudo apt install lynis
```

## Common Commands

```bash
sudo lynis audit system
sudo lynis show details
cat /var/log/lynis-report.dat | grep suggestion
```

## Lab Exercise

Run `lynis audit system` on every server image before it goes into production, and again on a recurring cron so drift gets caught, not just the initial build. In your lab, run it on a fresh VM, fix the top 3 suggestions, and re-run to confirm the score improves.

## Related Tools

- [OpenSCAP](openscap.md) — heavier compliance-framework alternative
- [rkhunter](rkhunter.md) — complementary rootkit-focused scan
