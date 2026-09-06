# AIDE

File and directory integrity checker — builds a baseline database of file hashes/attributes and flags anything that changes since.

**Links:** [GitHub](https://github.com/aide/aide) · [Docs](https://aide.github.io)

## Overview

AIDE is a lightweight, standalone file-integrity monitor (similar in concept to what Wazuh's FIM module or Tripwire provide) — build a baseline after a clean install, then run periodic checks to detect unexpected file changes (a classic sign of a compromised host).

## Install / Deploy

```bash
sudo apt install aide
sudo aideinit   # build the initial baseline database
```

## Common Commands

```bash
sudo aide --check
sudo aide --update   # after an intentional change, refresh the baseline
```

## Lab Exercise

Build an AIDE baseline on a lab VM, modify a system file (e.g. add a line to `/etc/passwd` or plant a test binary in `/usr/bin`), and confirm `aide --check` flags the change.

## Related Tools

- [rkhunter](rkhunter.md) — complementary rootkit-focused scan
- [Wazuh](../../detect-and-respond/tools/wazuh.md) — has its own built-in file-integrity monitoring
