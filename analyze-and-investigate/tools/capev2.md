# CAPEv2

Automated malware analysis sandbox (Cuckoo successor) — detonates a submitted sample in an instrumented VM and reports behavior: network calls, file/registry changes, and unpacked payloads.

**Links:** [GitHub](https://github.com/kevoreilly/CAPEv2) · [Docs](https://capev2.readthedocs.io)

## Overview

CAPE extends Cuckoo Sandbox with better unpacking/config-extraction capability, giving you not just "what did the malware do" but often the actual C2 configuration extracted from memory. Submissions run inside isolated VMs that snapshot back to clean state after each detonation.

## Install / Deploy

```bash
git clone https://github.com/kevoreilly/CAPEv2.git
cd CAPEv2 && sudo ./installer/cape2.sh base
sudo ./installer/cape2.sh cape
```

## Common Commands

```bash
python3 utils/submit.py /path/to/sample.exe
python3 utils/process.py -r <task-id>
```

## Lab Exercise

Submit a captured sample (e.g. from [Dionaea](../../detect-and-respond/tools/dionaea.md)) to a CAPE instance running on an isolated hypervisor VLAN, and review the resulting report for network indicators you could feed into [MISP](../../detect-and-respond/tools/misp.md).

## Related Tools

- [Cuckoo Sandbox](cuckoo-sandbox.md) — the project CAPE forked from
- [YARA](yara.md) — used internally for sample classification
- [REMnux](remnux.md) — manual analysis complement
