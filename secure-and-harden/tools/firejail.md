# Firejail

SUID sandbox that restricts what a Linux application can touch — namespace-based sandboxing for individual applications without needing full containers.

**Links:** [GitHub](https://github.com/netblue30/firejail) · [Docs](https://firejail.wordpress.com)

## Overview

Firejail wraps a single application in restricted Linux namespaces, limiting its filesystem/network access — a lightweight way to reduce the blast radius of a risky application (a PDF reader, a browser, an untrusted script) without the overhead of a full container or VM.

## Install / Deploy

```bash
sudo apt install firejail
```

## Common Commands

```bash
firejail firefox
firejail --net=none ./untrusted_script.sh
firejail --private firefox   # ephemeral home directory
```

## Lab Exercise

Run a PDF viewer or browser under Firejail with `--net=none` and confirm it genuinely can't make outbound connections — a useful sanity check before trusting the sandbox for something riskier.

## Related Tools

- [REMnux](../../analyze-and-investigate/tools/remnux.md) — heavier isolated-VM alternative for genuinely risky analysis
