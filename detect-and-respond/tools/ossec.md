# OSSEC

Open-source host-based intrusion detection — log analysis, file-integrity monitoring, and rootkit detection running as an agent on each protected host.

**Links:** [GitHub](https://github.com/ossec/ossec-hids) · [Docs](https://www.ossec.net/docs/)

## Overview

OSSEC is the host-based counterpart to network tools like Suricata/Zeek — it watches local logs, file changes, and running processes on the box it's installed on. Wazuh is a fork of OSSEC with a modern stack layered on top, so most new deployments choose Wazuh unless there's a specific reason to run OSSEC directly.

## Install / Deploy

```bash
# Manager:
wget https://github.com/ossec/ossec-hids/archive/refs/tags/3.7.0.tar.gz
tar -xzf 3.7.0.tar.gz && cd ossec-hids-3.7.0 && sudo ./install.sh
```

## Common Commands

```bash
sudo /var/ossec/bin/ossec-control status
sudo /var/ossec/bin/manage_agents
tail -f /var/ossec/logs/alerts/alerts.log
```

## Lab Exercise

Install OSSEC on a lab VM, modify a monitored file (e.g. `/etc/passwd`), and confirm a file-integrity alert fires in `alerts.log` — then compare the experience against deploying [Wazuh](wazuh.md) for the same check.

## Related Tools

- [Wazuh](wazuh.md) — modern fork with a full SIEM stack layered on top
