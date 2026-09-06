# Keycloak

Enterprise-grade open-source identity and access management — Red Hat-backed, the most mature/feature-complete free IdP option.

**Links:** [GitHub](https://github.com/keycloak/keycloak) · [Docs](https://www.keycloak.org/documentation)

## Overview

Keycloak covers the same ground as Authentik (SAML, OAuth2/OIDC, LDAP federation) with a longer track record in enterprise environments — a reasonable choice if you're specifically practicing skills that transfer to enterprise IAM work rather than picking the lightest homelab option.

## Install / Deploy

```bash
docker run -d -p 8080:8080 -e KEYCLOAK_ADMIN=admin -e KEYCLOAK_ADMIN_PASSWORD=admin \
  quay.io/keycloak/keycloak:latest start-dev
```

## Common Commands

Web-UI driven admin console (`http://localhost:8080`); configure Realms, Clients, and Users through the interface, or automate via the REST Admin API.

## Lab Exercise

Deploy Keycloak, create a Realm and an OIDC client for a homelab app, and compare the admin-console workflow against setting up the same OIDC integration in [Authentik](authentik.md).

## Related Tools

- [Authentik](authentik.md) — comparable, often considered friendlier for homelab use
