# Elastic Stack / Elastic Security

Free-tier SIEM detections on top of the ELK stack (Elasticsearch, Logstash, Kibana) — Elastic's own detection-rules repo gives you a starting ruleset without building from scratch.

**Links:** [GitHub (detection rules)](https://github.com/elastic/detection-rules) · [Docs](https://www.elastic.co/guide/en/security/current/index.html)

## Overview

Elastic Security layers SIEM-style detection rules, timeline investigation, and case management on top of the free/open Elastic Stack — a reasonable choice if you're already running Elasticsearch for logging and want detection capability without adding a second platform.

## Install / Deploy

```bash
docker network create elastic
docker run -d --name es01 --net elastic -p 9200:9200 docker.elastic.co/elasticsearch/elasticsearch:8.15.0
docker run -d --name kib01 --net elastic -p 5601:5601 docker.elastic.co/kibana/kibana:8.15.0
```

## Common Commands

```bash
git clone https://github.com/elastic/detection-rules.git
# import rules via Kibana's Security app → Rules → Import
```

## Lab Exercise

Ship Sysmon logs from a lab Windows VM into Elasticsearch (via Winlogbeat), import a handful of Elastic's prebuilt detection rules, and confirm one fires against a known-bad action like [Mimikatz](../../test-and-exploit/tools/mimikatz.md).

## Related Tools

- [Sigma](sigma.md) — vendor-agnostic rules, convertible to Elastic's query language via [Uncoder IO](../../threat-intel-and-reference/tools/uncoder-io.md)
- [Graylog](graylog.md) — lighter-weight log-management alternative
