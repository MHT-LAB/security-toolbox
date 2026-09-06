# Pi-hole

Network-wide DNS filtering and ad blocking — a DNS sinkhole that blocks ad/tracker domains for every device on the network, not just one browser.

**Links:** [GitHub](https://github.com/pi-hole/pi-hole) · [Docs](https://docs.pi-hole.net)

## Overview

Pi-hole runs as your network's DNS resolver, blocking known ad/tracker/malware domains at the DNS level before they ever load — works for every device on the network (phones, smart TVs, IoT) without installing anything per-device, and gives a dashboard of exactly what's being queried.

## Install / Deploy

```bash
curl -sSL https://install.pi-hole.net | bash
# or Docker:
docker run -d -p 53:53/tcp -p 53:53/udp -p 80:80 --name pihole pihole/pihole
```

## Common Commands

```bash
pihole -up          # update
pihole -g            # update gravity (blocklists)
pihole -q example.com   # query whether a domain is blocked
```

## Lab Exercise

Point your router's DHCP DNS setting at Pi-hole, browse a few ad-heavy sites, and review the Pi-hole dashboard's query log to see what got blocked — then add a custom blocklist and confirm it takes effect after `pihole -g`.

## Related Tools

- [Unbound](unbound.md) — pair with Pi-hole as a recursive resolver instead of relying on an upstream DNS provider
