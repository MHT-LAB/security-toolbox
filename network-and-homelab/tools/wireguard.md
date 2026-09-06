# WireGuard

The modern, lightweight VPN protocol underneath Tailscale and most of the network stack in this folder.

**Links:** [GitHub](https://github.com/WireGuard/wireguard-linux) · [Docs](https://www.wireguard.com/quickstart/)

## Overview

WireGuard is a minimal, fast, cryptographically modern VPN protocol — a fraction of the code size of OpenVPN/IPsec, which makes it easier to audit and faster in practice. Most modern mesh-VPN products (Tailscale, Netmaker) are built directly on it.

## Install / Deploy

```bash
sudo apt install wireguard
wg genkey | tee privatekey | wg pubkey > publickey
```

## Common Commands

```bash
sudo wg-quick up wg0
sudo wg show
sudo wg-quick down wg0
```

## Lab Exercise

Configure a raw WireGuard tunnel by hand between two lab VMs (rather than using Tailscale's managed layer) to understand what Tailscale/Netmaker are actually automating underneath — generate keys, write the config, and bring the tunnel up manually.

## Related Tools

- [Tailscale](tailscale.md) · [Netmaker](netmaker.md) — managed mesh layers built on this protocol
