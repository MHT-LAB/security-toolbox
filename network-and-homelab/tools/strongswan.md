# strongSwan

Open-source IPsec VPN implementation — the standard choice for site-to-site VPN tunnels and IKEv2 client VPN, common where IPsec is required for interoperability.

**Links:** [GitHub](https://github.com/strongswan/strongswan) · [Docs](https://docs.strongswan.org)

## Overview

Where WireGuard/OpenVPN are the go-to for personal/remote-access VPN, strongSwan's IPsec/IKEv2 implementation is what you reach for when interoperating with commercial firewalls/routers that expect standard IPsec — common in site-to-site VPN scenarios between different vendors' equipment.

## Install / Deploy

```bash
sudo apt install strongswan
```

## Common Commands

```bash
sudo ipsec restart
sudo ipsec status
sudo ipsec up <connection-name>
```

## Lab Exercise

Configure a site-to-site IPsec tunnel between two lab OPNsense/pfSense firewalls using strongSwan's IKEv2, and confirm traffic routes correctly between the two "sites."

## Related Tools

- [OpenVPN](openvpn.md) — SSL-based alternative
- [OPNsense](../../secure-and-harden/tools/opnsense.md) — commonly the firewall managing the IPsec tunnel
