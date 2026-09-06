# Greenbone Community Edition (OpenVAS)

Free vulnerability scanning engine — full-featured network vulnerability scanner with regularly-updated feed data.

**Links:** [GitHub](https://github.com/greenbone/openvas-scanner) · [Docs](https://greenbone.github.io/docs/)

## Overview

Greenbone/OpenVAS provides broad, feed-driven vulnerability scanning (tens of thousands of checks) with a web UI (Greenbone Security Assistant) for managing scans and reviewing results — the closest free equivalent to a commercial vulnerability scanner like Nessus.

## Install / Deploy

```bash
# Official Docker Compose deployment:
git clone https://github.com/greenbone/openvas-docker.git
cd openvas-docker && docker-compose up -d
```

## Common Commands

Greenbone is primarily web-UI driven; scans are configured and reviewed through the Greenbone Security Assistant interface at `https://localhost:9392`.

## Lab Exercise

Deploy Greenbone against your lab network, run a full scan against [Metasploitable3](../../test-and-exploit/tools/metasploitable3.md), and cross-reference its findings against what you already know is vulnerable on that box from earlier [Nmap](../../recon-and-osint/tools/nmap.md)/[Metasploit](../../test-and-exploit/tools/metasploit.md) work.

## Related Tools

- [Vuls](vuls.md) — lighter-weight, agentless alternative
- [Nmap](../../recon-and-osint/tools/nmap.md) — complementary discovery step
