# Authentik

Full-featured self-hosted identity provider (SSO, SAML, OAuth2) — heavier than Authelia, aimed at acting as a genuine central IdP rather than just a proxy-auth gate.

**Links:** [GitHub](https://github.com/goauthentik/authentik) · [Docs](https://docs.goauthentik.io)

## Overview

Authentik provides real identity-provider protocols (SAML, OAuth2/OIDC, LDAP) so it can be the actual login backend for applications that support those standards, not just a forward-auth gate in front of apps that don't — a step up from Authelia when you want proper federated login.

## Install / Deploy

```bash
git clone https://github.com/goauthentik/authentik.git
cd authentik && docker compose up -d
```

## Common Commands

Web-UI driven; configure "Providers" (OAuth2/SAML) and "Applications" through the admin interface.

## Lab Exercise

Deploy Authentik and configure it as an OIDC provider for a homelab app that supports OIDC login (e.g. Grafana), then confirm you can log into Grafana using Authentik-issued credentials.

## Related Tools

- [Authelia](authelia.md) — lighter forward-auth alternative
- [Keycloak](keycloak.md) — comparable enterprise-grade alternative
