# HELK

Elastic-based hunting platform with Spark/Jupyter for advanced analytics — built for threat hunters who want to run notebook-style analysis over Sysmon/Zeek data.

**Links:** [GitHub](https://github.com/Cyb3rWard0g/HELK)

## Overview

HELK bundles Elasticsearch/Kibana with Apache Spark and Jupyter notebooks, aimed at hunters who want to run statistical/graph analysis over collected telemetry rather than just dashboard-and-alert workflows — a research-oriented step up from a standard SIEM setup.

## Install / Deploy

```bash
git clone https://github.com/Cyb3rWard0g/HELK.git
cd HELK/docker && sudo ./helk_install.sh
```

## Common Commands

HELK is primarily accessed through Kibana and Jupyter web UIs; once deployed:
```text
Jupyter: http://<helk-ip>:8880
Kibana:  http://<helk-ip>:5601
```

## Lab Exercise

Ship Sysmon logs from a lab Windows VM into HELK, then use a Jupyter notebook to run a simple frequency analysis (e.g. rarest parent-child process pairs) — a good introduction to hunting beyond keyword search.

## Related Tools

- [Sysmon config](sysmon-config.md) — typical data source
- [Elastic Stack](elastic-stack.md) — the base HELK builds on
