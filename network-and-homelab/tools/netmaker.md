# Netmaker

WireGuard-based mesh network management at scale — a self-hosted alternative to Tailscale when you want to run your own control plane instead of using Tailscale's hosted coordination.

**Links:** [GitHub](https://github.com/gravitl/netmaker)

## Overview

Netmaker automates WireGuard mesh configuration (like Tailscale) but is fully self-hosted — you run the control server yourself rather than depending on a third party's coordination service, at the cost of more setup/maintenance.

## Install / Deploy

```bash
wget -qO - https://raw.githubusercontent.com/gravitl/netmaker/master/scripts/nm-quick.sh | sudo bash
```

## Common Commands

Netmaker is primarily web-UI/API driven; nodes join a network via a generated enrollment key.

## Lab Exercise

Deploy a Netmaker server, join two lab VMs to a network, and compare the self-hosted control-plane experience against [Tailscale](tailscale.md)'s hosted coordination for the same mesh setup.

## Related Tools

- [Tailscale](tailscale.md) — hosted alternative built on the same underlying protocol
- [WireGuard](wireguard.md) — the protocol both automate
