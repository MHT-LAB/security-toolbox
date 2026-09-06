# GreyNoise (pygreynoise)

API client for filtering internet background noise out of alerts — tells you whether an IP hitting your systems is a known mass-scanner rather than a targeted actor.

**Links:** [GitHub](https://github.com/GreyNoise-Intelligence/pygreynoise) — free-tier SaaS API.

## Overview

A huge fraction of "attacker" IPs seen in any internet-facing log are just internet-wide scanners (Shodan, Censys, research projects, botnets) rather than anything targeted at you specifically. GreyNoise's API tells you which is which, letting you deprioritize alerts on known mass-scanners.

## Install / Deploy

```bash
pip install greynoise
export GREYNOISE_API_KEY=your_key
```

## Common Commands

```bash
greynoise ip 1.2.3.4
greynoise quick 1.2.3.4 5.6.7.8    # bulk quick lookup
```

## Lab Exercise

Take a batch of source IPs from your Suricata/Wazuh alert logs and check them against GreyNoise's API — filter out anything tagged as a known benign/mass scanner and see how much alert volume that removes.

## Related Tools

- [AbuseIPDB](../../recon-and-osint/tools/abuseipdb.md) — complementary reputation lookup
