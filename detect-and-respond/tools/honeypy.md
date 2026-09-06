# HoneyPy

Low-interaction Python honeypot, easy to extend with new service plugins.

**Links:** [GitHub](https://github.com/foospidy/HoneyPy)

## Overview

HoneyPy is a simple, plugin-based low-interaction honeypot — easier to read and extend than heavier frameworks, making it a reasonable starting point if you want to write a custom service emulation yourself.

## Install / Deploy

```bash
git clone https://github.com/foospidy/HoneyPy.git
cd HoneyPy && pip install -r requirements.txt
python3 HoneyPy.py
```

## Common Commands

```bash
python3 HoneyPy.py
tail -f logs/honeypy.log
```

## Lab Exercise

Enable one of HoneyPy's simpler service plugins (e.g. a fake Telnet banner) on a lab VM and confirm interactions get logged — then try writing a one-off plugin for a service specific to your homelab.

## Related Tools

- [HoneyTrap](honeytrap.md) — similar framework-for-building-honeypots approach
