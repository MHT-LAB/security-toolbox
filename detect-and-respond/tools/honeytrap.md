# HoneyTrap

Modular, extensible honeypot framework for building custom low/medium-interaction traps.

**Links:** [GitHub](https://github.com/honeytrap/honeytrap)

## Overview

HoneyTrap is less a single honeypot than a framework for building one — pluggable "listeners" and "services" let you emulate whatever protocol or service you need, when the pre-built honeypots (Cowrie, Dionaea) don't cover your specific use case.

## Install / Deploy

```bash
git clone https://github.com/honeytrap/honeytrap.git
cd honeytrap && make
./honeytrap --config config.toml
```

## Common Commands

```bash
./honeytrap --config config.toml
```

## Lab Exercise

Configure HoneyTrap to emulate a service specific to your homelab's actual exposed surface (rather than a generic template), and compare the realism/detail of its logs against a pre-built honeypot like Cowrie for a similar protocol.

## Related Tools

- [Cowrie](cowrie.md) · [Dionaea](dionaea.md) — pre-built alternatives for common protocols
