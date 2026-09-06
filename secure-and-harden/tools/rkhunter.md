# rkhunter

Rootkit, backdoor, and local exploit scanner for *nix hosts — checks system binaries against known-good signatures and looks for common rootkit indicators.

**Links:** [GitHub](https://github.com/Rootkit-Hunter/rkhunter) · [Docs](https://rkhunter.sourceforge.net)

## Overview

rkhunter checks for signs of rootkits — modified system binaries, hidden files/directories, suspicious kernel modules — and can be run on a schedule as part of routine host hardening verification.

## Install / Deploy

```bash
sudo apt install rkhunter
sudo rkhunter --update
sudo rkhunter --propupd   # baseline file properties after a clean install
```

## Common Commands

```bash
sudo rkhunter --check
sudo rkhunter --check --sk   # skip interactive prompts, for cron use
```

## Lab Exercise

Run `rkhunter --check` on a fresh lab VM to establish a clean baseline, then re-run after installing something unusual (a kernel module, an unsigned binary) to see what triggers a warning.

## Related Tools

- [AIDE](aide.md) — complementary file-integrity approach
- [ClamAV](clamav.md) — complementary signature-based malware scan
