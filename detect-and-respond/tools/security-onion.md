# Security Onion

Linux distro purpose-built for network security monitoring and threat hunting — bundles Suricata, Zeek, and Elastic-based analysis tools into one deployable platform.

**Links:** [GitHub](https://github.com/Security-Onion-Solutions/securityonion) · [Docs](https://docs.securityonion.net)

## Overview

Rather than assembling Suricata, Zeek, and a SIEM by hand, Security Onion ships them integrated on one ISO, with a setup wizard for standalone or distributed deployments and a unified Kibana-based interface for hunting across all the ingested data.

## Install / Deploy

```text
Download the ISO from securityonionsolutions.com/download and install to
dedicated hardware or a VM with a SPAN/mirror port feeding its monitor interface.
Run `sudo sosetup` to configure standalone vs distributed mode.
```

## Common Commands

```bash
sudo so-status              # check all service health
sudo so-allow                # open firewall access for analyst IPs
sudo so-import-pcap file.pcap   # import a pcap for offline analysis
```

## Lab Exercise

Deploy as a standalone VM with a mirrored port from your homelab switch, generate some traffic (e.g. an Nmap scan from another VM), and confirm the resulting alerts appear correctly attributed in the dashboard.

## Related Tools

- [Suricata](suricata.md) · [Zeek](zeek.md) — the engines it bundles
- [Arkime](arkime.md) — complementary full-packet-capture indexing
