# T-Pot

Deutsche Telekom's all-in-one honeypot platform, bundling 20+ honeypots (Cowrie, Dionaea, Conpot, and more) behind one dashboard.

**Links:** [GitHub](https://github.com/telekom-security/tpot) · [Docs](https://github.com/telekom-security/tpot/blob/master/README.md)

## Overview

Rather than deploying each honeypot separately, T-Pot bundles them all in Docker containers with a unified Elastic-based dashboard (Kibana) for viewing hits across every honeypot type at once — a fast way to get real-world attack telemetry running.

## Install / Deploy

```bash
git clone https://github.com/telekom-security/tpot.git
cd tpot/iso/installer && sudo ./install.sh
# Or install directly on Debian: see repo's install docs
```

## Common Commands

Management is via the bundled web dashboard and `docker ps`/`docker logs` for individual honeypot containers.

## Lab Exercise

Stand up T-Pot on an isolated VM with a public-facing IP (never on a segment with anything that matters), and after 24 hours review the Kibana dashboard's attack map and top-attacker list — real internet scanning traffic finds it fast.

## Related Tools

- [Cowrie](cowrie.md) · [Dionaea](dionaea.md) · [Conpot](conpot.md) — individually, some of the honeypots T-Pot bundles
