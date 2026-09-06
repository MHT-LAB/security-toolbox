# YARA

Pattern-matching for identifying and classifying malware — write rules describing strings/byte patterns/conditions, then scan files or memory for matches.

**Links:** [GitHub](https://github.com/VirusTotal/yara) · [Docs](https://yara.readthedocs.io)

## Overview

YARA rules describe "what malware family X looks like" in terms of strings, hex patterns, and boolean conditions — VirusTotal, most sandboxes (CAPEv2), and many EDR products use YARA rules as a core detection mechanism. Writing your own rules is a standard malware-analysis skill.

## Install / Deploy

```bash
sudo apt install yara
```

## Common Commands

```bash
yara rule.yar suspicious_file.exe
yara -r rules_directory/ /path/to/scan/
```

## Lab Exercise

Write a simple YARA rule matching a unique string from a sample captured by [Dionaea](../../detect-and-respond/tools/dionaea.md) or downloaded from [MalwareBazaar](../../threat-intel-and-reference/tools/abusech.md), then confirm it correctly flags that sample and doesn't false-positive on a clean file.

## Related Tools

- [Loki](loki.md) · [Fenrir](fenrir.md) — IOC scanners built around YARA
- [CAPEv2](capev2.md) — sandbox that uses YARA rules for classification
