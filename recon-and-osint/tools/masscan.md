# Masscan

Internet-scale port scanner — orders of magnitude faster than Nmap for broad sweeps, at the cost of the deep service-detection Nmap provides.

**Links:** [GitHub](https://github.com/robertdavidgraham/masscan) · [Docs](https://github.com/robertdavidgraham/masscan#usage)

## Overview

Masscan uses its own TCP/IP stack to blast SYN packets asynchronously, making it capable of scanning the entire IPv4 space in minutes given enough bandwidth. It's a first-pass "what's open" tool — hand results to Nmap for the detailed follow-up.

## Install / Deploy

```bash
sudo apt install masscan
```

## Common Commands

```bash
sudo masscan -p1-65535 10.0.0.0/24 --rate=1000
sudo masscan -p80,443 10.0.0.0/16 --rate=10000 -oL results.txt
```

## Lab Exercise

Scan your lab subnet with Masscan at a conservative `--rate` first, then feed any open ports found into a targeted `nmap -sV -p<ports>` scan on just those hosts — this two-stage pattern is how most large-scope engagements actually work.

## Related Tools

- [Nmap](nmap.md) — detailed follow-up scan on whatever Masscan finds open
