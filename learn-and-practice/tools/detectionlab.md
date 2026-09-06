# DetectionLab

Vagrant/Packer-built AD lab pre-wired with logging/detection tooling — ideal for practicing blue-team work end to end, not just attacking.

**Links:** [GitHub](https://github.com/clong/DetectionLab)

## Overview

DetectionLab stands up a small Active Directory domain (DC, Windows workstation, Linux logging host) with Sysmon, Splunk/ELK, and Zeek already configured — so you can generate attacker activity and immediately see what your detection stack catches, without spending hours on setup first.

## Install / Deploy

```bash
git clone https://github.com/clong/DetectionLab.git
cd DetectionLab/Vagrant && ./build.sh virtualbox
```

## Common Commands

Managed via Vagrant (`vagrant up`, `vagrant halt`); day-to-day analysis is through the bundled Splunk/ELK web UI.

## Lab Exercise

Build DetectionLab, run [Mimikatz](../../test-and-exploit/tools/mimikatz.md) or [Responder](../../test-and-exploit/tools/responder.md) against the domain-joined workstation, and confirm the pre-configured Sysmon/Splunk setup actually shows the resulting events.

## Related Tools

- [GOAD](goad.md) — comparable AD lab, more focused on attack-path complexity than logging
- [Sysmon config](../../detect-and-respond/tools/sysmon-config.md) — what DetectionLab ships pre-configured
