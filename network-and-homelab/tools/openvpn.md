# OpenVPN

The long-standing standard SSL VPN, still widely deployed — SSL/TLS-based VPN protocol, predates WireGuard and remains common in enterprise environments.

**Links:** [GitHub](https://github.com/OpenVPN/openvpn) · [Docs](https://openvpn.net/community-resources/)

## Overview

OpenVPN is heavier and slower than WireGuard but has a longer enterprise track record and broader legacy-client support — worth knowing even in a WireGuard-first homelab, since many corporate/client VPN setups you'll encounter professionally still run it.

## Install / Deploy

```bash
docker run -v ./ovpn-data:/etc/openvpn --rm kylemanna/openvpn ovpn_genconfig -u udp://VPN.SERVERNAME.COM
docker run -v ./ovpn-data:/etc/openvpn -p 1194:1194/udp kylemanna/openvpn
```

## Common Commands

```bash
openvpn --config client.ovpn
```

## Lab Exercise

Stand up an OpenVPN server in your lab and connect a client, then compare setup complexity and connection speed against the [WireGuard](wireguard.md) tunnel from that earlier lab exercise.

## Related Tools

- [WireGuard](wireguard.md) — modern, faster alternative
- [strongSwan](strongswan.md) — IPsec-based alternative, common in site-to-site scenarios
