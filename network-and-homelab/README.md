# Network & Homelab

Self-hosted infrastructure — what's actually running the lab.

## 🏆 Top 15 (most widely used)

- **[Tailscale](https://github.com/tailscale/tailscale)** — mesh VPN built on WireGuard; free tier covers a homelab easily.
  *Use it:* put it on every homelab box first, before exposing anything else to the internet — it collapses "how do I remotely reach this" into one solved problem.
- **[WireGuard](https://github.com/WireGuard/wireguard-linux)** — the modern, lightweight VPN protocol underneath Tailscale and most of the above.
- **[Proxmox VE](https://www.proxmox.com/en/proxmox-virtual-environment/overview)** — free type-1 hypervisor for running everything else; source hosted on Proxmox's own GitLab, no primary GitHub mirror.
- **[TrueNAS](https://github.com/truenas/middleware)** — free NAS operating system (CORE/SCALE).
- **[OPNsense](https://github.com/opnsense/core)** — free, open-source firewall and router platform.
- **[Pi-hole](https://github.com/pi-hole/pi-hole)** — network-wide DNS filtering and ad blocking.
- **[Portainer CE](https://github.com/portainer/portainer)** — free Docker/container management UI.
- **[Uptime Kuma](https://github.com/louislam/uptime-kuma)** — self-hosted uptime monitoring with a clean dashboard.
- **[Netdata](https://github.com/netdata/netdata)** — real-time infrastructure and performance monitoring.
- **[Docker Compose](https://github.com/docker/compose)** — the standard way most of this list actually gets deployed in a homelab.
- **[Nginx Proxy Manager](https://github.com/NginxProxyManager/nginx-proxy-manager)** — GUI-managed reverse proxy with automatic Let's Encrypt certs.
- **[Traefik](https://github.com/traefik/traefik)** — cloud-native reverse proxy/load balancer with automatic service discovery.
- **[Grafana](https://github.com/grafana/grafana)** — dashboarding for metrics from Prometheus, Netdata, and friends.
- **[Prometheus](https://github.com/prometheus/prometheus)** — the standard open-source metrics collection and alerting engine.
- **[Zabbix](https://github.com/zabbix/zabbix)** — full-featured infrastructure monitoring, deeper than Uptime Kuma when you outgrow it.

## More tools worth knowing

- **[Vaultwarden](https://github.com/dani-garcia/vaultwarden)** — lightweight self-hosted Bitwarden-compatible password manager server.
- **[Authelia](https://github.com/authelia/authelia)** — self-hosted SSO/2FA authentication portal for reverse-proxied services.
- **[Authentik](https://github.com/goauthentik/authentik)** — full-featured self-hosted identity provider (SSO, SAML, OAuth2).
- **[Keycloak](https://github.com/keycloak/keycloak)** — enterprise-grade open-source identity and access management.
- **[OpenVPN](https://github.com/OpenVPN/openvpn)** — the long-standing standard SSL VPN, still widely deployed.
- **[strongSwan](https://github.com/strongswan/strongswan)** — open-source IPsec VPN implementation.
- **[Netmaker](https://github.com/gravitl/netmaker)** — WireGuard-based mesh network management at scale.
- **[Cockpit](https://github.com/cockpit-project/cockpit)** — web-based admin console for managing Linux servers.
- **[NetBox](https://github.com/netbox-community/netbox)** — IPAM/DCIM tool for tracking network documentation as data, not a spreadsheet.
- **[LibreNMS](https://github.com/librenms/librenms)** — auto-discovering network monitoring platform (SNMP-based).
- **[ntopng](https://github.com/ntop/ntopng)** — real-time network traffic monitoring and visualization.
- **[Unbound](https://github.com/NLnetLabs/unbound)** — validating, recursive, caching DNS resolver.
- **[FreeIPA](https://github.com/freeipa/freeipa)** — open-source identity, policy, and audit management for Linux/Unix environments.
- **[Semaphore UI](https://github.com/semaphoreui/semaphore)** — web UI for running and scheduling Ansible playbooks.

*General infrastructure guidance:* put everything behind Tailscale or a reverse proxy with Authelia/Authentik in front rather than port-forwarding services directly to the internet; run Prometheus/Grafana or Netdata from day one so a hardening or detection tool later has a baseline to compare against.
