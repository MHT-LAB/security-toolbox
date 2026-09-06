# Sysmon config (SwiftOnSecurity)

Battle-tested Sysmon configuration for meaningful Windows telemetry — Sysmon itself ships with almost no useful default config, this fills that gap.

**Links:** [GitHub](https://github.com/SwiftOnSecurity/sysmon-config)

## Overview

Sysmon (a free Microsoft Sysinternals tool) logs detailed process, network, and file-system events, but its out-of-the-box configuration captures almost nothing useful. This community-maintained config is the de facto starting point almost every Windows detection engineering effort builds on.

## Install / Deploy

```powershell
# Download Sysmon from Microsoft Sysinternals, then:
sysmon64.exe -accepteula -i sysmonconfig-export.xml
```

## Common Commands

```powershell
sysmon64 -c sysmonconfig-export.xml   # update running config
Get-WinEvent -LogName "Microsoft-Windows-Sysmon/Operational" -MaxEvents 20
```

## Lab Exercise

Install Sysmon with this config on a lab Windows VM, run [Mimikatz](../../test-and-exploit/tools/mimikatz.md), and confirm Sysmon Event ID 10 (process access to LSASS) is logged — then feed that log into [Wazuh](wazuh.md) or [Zircolite](zircolite.md).

## Related Tools

- [Wazuh](wazuh.md) · [Elastic Stack](elastic-stack.md) — where these logs typically end up
- [Zircolite](zircolite.md) — Sigma-rule matching against the resulting events
