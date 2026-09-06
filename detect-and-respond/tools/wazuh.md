# Wazuh

Free, open-source SIEM and XDR platform — agents on endpoints feed a central manager that correlates logs, file-integrity events, and vulnerability data into alerts.

**Links:** [GitHub](https://github.com/wazuh/wazuh) · [Docs](https://documentation.wazuh.com)

## Overview

Wazuh is the most complete free SIEM/XDR on this list: log collection, file-integrity monitoring, rootkit detection, vulnerability detection, and a rule engine, all with a Kibana-based dashboard (Wazuh indexer/dashboard). It's the natural default for a homelab or small-org SOC stack.

## Install / Deploy

```bash
# Single-node quickstart (manager + indexer + dashboard):
curl -sO https://packages.wazuh.com/4.9/wazuh-install.sh
sudo bash wazuh-install.sh -a

# Agent enrollment on an endpoint:
sudo WAZUH_MANAGER='<manager-ip>' apt-get install wazuh-agent
```

## Common Commands

```bash
sudo systemctl status wazuh-manager
sudo /var/ossec/bin/agent_control -l          # list connected agents
sudo /var/ossec/bin/manage_agents             # add/remove agents
```

## Lab Exercise

Deploy the manager as a VM, enroll two or three lab endpoints as agents, then trigger a known-bad action (e.g. run [Mimikatz](../../test-and-exploit/tools/mimikatz.md) on one) and confirm an alert fires — tune the relevant rule if it's too noisy or silent before moving on.

## Related Tools

- [TheHive](thehive.md) — route alerts here for case management
- Sysmon config ([SwiftOnSecurity](sysmon-config.md)) — improves what Wazuh has to alert on
