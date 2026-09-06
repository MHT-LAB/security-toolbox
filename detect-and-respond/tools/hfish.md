# HFish

Free honeypot deployment/management platform with a wide range of service probes and a central dashboard.

**Links:** [GitHub](https://github.com/hacklcx/HFish)

## Overview

HFish provides a central management console for deploying many lightweight honeypot probes across an environment, aimed at teams that want an OpenCanary-like central-alerting experience with a broader range of pre-built service templates.

## Install / Deploy

```bash
# Download release binary for your platform from the GitHub releases page
./hfish-manager   # central management console
./hfish-node      # deployed honeypot probe
```

## Common Commands

Managed primarily through HFish's web dashboard once the manager and node components are running.

## Lab Exercise

Deploy the HFish manager plus one probe node on a spare lab VM, enable a couple of service templates, and confirm alerts reach the central dashboard when probed — compare the management-console experience against running [OpenCanary](opencanary.md) standalone.

## Related Tools

- [OpenCanary](opencanary.md) — simpler single-host alternative
