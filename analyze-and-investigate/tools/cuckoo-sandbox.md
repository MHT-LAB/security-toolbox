# Cuckoo Sandbox

The original open-source automated malware sandbox CAPE forked from — still referenced and occasionally deployed where CAPE's additional complexity isn't needed.

**Links:** [GitHub](https://github.com/cuckoosandbox/cuckoo) · [Docs](https://cuckoosandbox.org/docs)

## Overview

Cuckoo established the pattern nearly every sandbox since has followed: submit a sample, detonate it in an instrumented VM, collect behavioral logs (API calls, network traffic, file/registry changes), and produce a report. Active development has largely moved to CAPE, but Cuckoo's codebase and concepts remain the reference starting point.

## Install / Deploy

```bash
pip install -U cuckoo
cuckoo init
cuckoo community    # download signatures
```

## Common Commands

```bash
cuckoo submit /path/to/sample.exe
cuckoo web runserver   # web UI for browsing reports
```

## Lab Exercise

If you want to understand sandbox internals before diving into CAPE's added complexity, install Cuckoo on an isolated lab host, submit a known-benign test file, and walk through the resulting report structure.

## Related Tools

- [CAPEv2](capev2.md) — actively maintained fork with more capability
