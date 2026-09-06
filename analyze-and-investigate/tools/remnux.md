# REMnux

Linux distro pre-loaded for malware analysis — a curated toolkit VM so you don't have to install and configure dozens of analysis tools yourself.

**Links:** [GitHub](https://github.com/REMnux/remnux) · [Docs](https://docs.remnux.org)

## Overview

REMnux ships as a distro/VM with static and dynamic analysis tools pre-installed and configured (network simulation, YARA, binwalk, and many others) — the standard base environment for hands-on malware analysis without building your own toolchain.

## Install / Deploy

```bash
# As an add-on to an existing Ubuntu install:
wget -q -O - https://remnux.org/install-remnux.py | sudo python3
# Or download the prebuilt VM image from remnux.org
```

## Common Commands

REMnux bundles many CLI tools already covered elsewhere in this folder — see individual pages ([YARA](yara.md), [binwalk](binwalk.md), [FLOSS](floss.md)) for their specific usage.

## Lab Exercise

Deploy REMnux as an isolated analysis VM (no route to production or the internet except through a controlled fake-DNS/inetsim setup), and use it as the base environment for the [YARA](yara.md) and [CAPEv2](capev2.md) lab exercises.

## Related Tools

- [YARA](yara.md) · [binwalk](binwalk.md) · [FLOSS](floss.md) — tools it bundles
- [CAPEv2](capev2.md) — complementary automated sandbox
