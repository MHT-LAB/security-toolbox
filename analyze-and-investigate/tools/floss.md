# FLOSS

Extracts obfuscated strings from malware binaries — goes beyond a basic `strings` dump by also recovering stack-based, encoded, and dynamically-constructed strings.

**Links:** [GitHub](https://github.com/mandiant/flare-floss)

## Overview

Malware authors routinely obfuscate strings (URLs, registry keys, C2 domains) to defeat a simple `strings` scan. FLOSS specifically hunts for and decodes these obfuscation techniques, often surfacing IOCs that a plain strings dump would completely miss.

## Install / Deploy

```bash
pip install flare-floss
```

## Common Commands

```bash
floss malware_sample.exe
floss --only static malware_sample.exe   # faster, static-only extraction
```

## Lab Exercise

Run plain `strings` and FLOSS against the same obfuscated test sample and compare the output — FLOSS should surface meaningful strings (URLs, registry paths) that the basic `strings` output misses entirely.

## Related Tools

- [CyberChef](cyberchef.md) — manually decode anything FLOSS partially recovers
- [binwalk](binwalk.md) — complementary for firmware/embedded binaries
