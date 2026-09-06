# Tailscale

Mesh VPN built on WireGuard — free tier covers a homelab easily, and it collapses "how do I remotely reach this" into one solved problem.

**Links:** [GitHub](https://github.com/tailscale/tailscale) · [Docs](https://tailscale.com/kb/)

## Overview

Tailscale creates a private mesh network between your devices using WireGuard under the hood, with NAT traversal and identity-based access handled for you — no port forwarding, no static IPs, and each device gets a stable name/IP reachable from anywhere.

## Install / Deploy

```bash
curl -fsSL https://tailscale.com/install.sh | sh
sudo tailscale up
```

## Common Commands

```bash
tailscale status
tailscale ping <device-name>
tailscale up --advertise-routes=192.168.1.0/24   # subnet router
```

## Lab Exercise

Install Tailscale on every homelab box first, before exposing anything else to the internet — join two lab VMs to your tailnet, then confirm you can reach one from the other (and from your laptop) without any port forwarding involved.

## Related Tools

- [WireGuard](wireguard.md) — the protocol underneath Tailscale
- [Authelia](authelia.md) · [Authentik](authentik.md) — add SSO on top once services are reachable
