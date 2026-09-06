# Network & Homelab

Self-hosted infrastructure — what's actually running the lab.

Every tool below has its own page under [`tools/`](tools/) with Overview, Install/Deploy, Common Commands, a concrete Lab Exercise, and Related Tools — not just a link out.

## 🏆 Top 15 (most widely used)

| Tool | What it does |
|---|---|
| [Tailscale](tools/tailscale.md) | Mesh VPN built on WireGuard; free tier covers a homelab easily. |
| [WireGuard](tools/wireguard.md) | The modern, lightweight VPN protocol underneath most of the above. |
| [Proxmox VE](tools/proxmox-ve.md) | Free type-1 hypervisor for running everything else. |
| [TrueNAS](tools/truenas.md) | Free NAS operating system (CORE/SCALE). |
| [OPNsense](../secure-and-harden/tools/opnsense.md) | Free, open-source firewall and router platform *(page under secure-and-harden)*. |
| [Pi-hole](tools/pi-hole.md) | Network-wide DNS filtering and ad blocking. |
| [Portainer CE](tools/portainer.md) | Free Docker/container management UI. |
| [Uptime Kuma](tools/uptime-kuma.md) | Self-hosted uptime monitoring with a clean dashboard. |
| [Netdata](tools/netdata.md) | Real-time infrastructure and performance monitoring. |
| [Docker Compose](tools/docker-compose.md) | The standard way most of this list actually gets deployed. |
| [Nginx Proxy Manager](tools/nginx-proxy-manager.md) | GUI-managed reverse proxy with automatic Let's Encrypt certs. |
| [Traefik](tools/traefik.md) | Cloud-native reverse proxy/load balancer with auto service discovery. |
| [Grafana](tools/grafana.md) | Dashboarding for metrics from Prometheus, Netdata, and friends. |
| [Prometheus](tools/prometheus.md) | The standard open-source metrics collection and alerting engine. |
| [Zabbix](tools/zabbix.md) | Full-featured infrastructure monitoring, deeper than Uptime Kuma. |

## More tools worth knowing

| Tool | What it does |
|---|---|
| [Vaultwarden](tools/vaultwarden.md) | Lightweight self-hosted Bitwarden-compatible password manager. |
| [Authelia](tools/authelia.md) | Self-hosted SSO/2FA authentication portal for reverse-proxied services. |
| [Authentik](tools/authentik.md) | Full-featured self-hosted identity provider (SSO, SAML, OAuth2). |
| [Keycloak](tools/keycloak.md) | Enterprise-grade open-source identity and access management. |
| [OpenVPN](tools/openvpn.md) | The long-standing standard SSL VPN, still widely deployed. |
| [strongSwan](tools/strongswan.md) | Open-source IPsec VPN implementation. |
| [Netmaker](tools/netmaker.md) | WireGuard-based mesh network management at scale, self-hosted. |
| [Cockpit](tools/cockpit.md) | Web-based admin console for managing Linux servers. |
| [NetBox](tools/netbox.md) | IPAM/DCIM tool for tracking network documentation as data. |
| [LibreNMS](tools/librenms.md) | Auto-discovering network monitoring platform (SNMP-based). |
| [ntopng](tools/ntopng.md) | Real-time network traffic monitoring and visualization. |
| [Unbound](tools/unbound.md) | Validating, recursive, caching DNS resolver. |
| [FreeIPA](tools/freeipa.md) | Open-source identity, policy, and audit management for Linux/Unix. |
| [Semaphore UI](tools/semaphore-ui.md) | Web UI for running and scheduling Ansible playbooks. |

*General infrastructure guidance:* put everything behind [Tailscale](tools/tailscale.md) or a reverse proxy with [Authelia](tools/authelia.md)/[Authentik](tools/authentik.md) in front rather than port-forwarding services directly to the internet; run [Prometheus](tools/prometheus.md)/[Grafana](tools/grafana.md) or [Netdata](tools/netdata.md) from day one so a hardening or detection tool later has a baseline to compare against.
