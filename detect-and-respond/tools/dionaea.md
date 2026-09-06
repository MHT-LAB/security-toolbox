# Dionaea

Malware-capturing honeypot that emulates vulnerable network services to collect dropped payloads.

**Links:** [GitHub](https://github.com/DinoTools/dionaea) · [Docs](https://dionaea.readthedocs.io)

## Overview

Dionaea emulates protocols commonly targeted by self-propagating malware (SMB, FTP, MSSQL, and more), and specifically captures any binary payload an attacker/worm tries to drop — useful both as a tripwire and as a source of fresh malware samples for [CAPEv2](../../analyze-and-investigate/tools/capev2.md) analysis.

## Install / Deploy

```bash
git clone https://github.com/DinoTools/dionaea.git
# Follow repo's build instructions (or use a prebuilt container image)
docker run -d -p 445:445 -p 21:21 dinotools/dionaea
```

## Common Commands

```bash
tail -f /opt/dionaea/var/log/dionaea/dionaea.log
ls /opt/dionaea/var/lib/dionaea/binaries/   # captured payloads
```

## Lab Exercise

Run Dionaea on an isolated lab segment for a period, then take any captured binary and run it through [CAPEv2](../../analyze-and-investigate/tools/capev2.md) or [VirusTotal](../../analyze-and-investigate/tools/virustotal.md) to identify what it is.

## Related Tools

- [CAPEv2](../../analyze-and-investigate/tools/capev2.md) — analyze whatever Dionaea captures
- [T-Pot](t-pot.md) — bundles Dionaea alongside many other honeypots
