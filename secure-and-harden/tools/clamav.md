# ClamAV

Open-source antivirus/malware-scanning engine — signature-based file scanning, commonly used on mail servers and file-upload pipelines rather than as an endpoint AV replacement.

**Links:** [GitHub](https://github.com/Cisco-Talos/clamav) · [Docs](https://docs.clamav.net)

## Overview

ClamAV is most useful embedded into a pipeline — scanning email attachments, uploaded files, or a periodic sweep of a file server — rather than as a full real-time endpoint AV. Cisco Talos maintains it and ships regular signature updates via `freshclam`.

## Install / Deploy

```bash
sudo apt install clamav clamav-daemon
sudo freshclam    # update signatures
```

## Common Commands

```bash
clamscan -r /path/to/scan
clamscan --infected --remove -r /uploads/
freshclam   # update virus definitions
```

## Lab Exercise

Set up ClamAV to scan a lab file-upload directory or mail spool, drop in the EICAR test file, and confirm it's detected and (in test mode) quarantined or flagged correctly.

## Related Tools

- [YARA](../../analyze-and-investigate/tools/yara.md) — complementary custom-rule-based detection
