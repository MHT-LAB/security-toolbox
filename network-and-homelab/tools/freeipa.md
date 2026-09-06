# FreeIPA

Open-source identity, policy, and audit management for Linux/Unix environments — combines LDAP, Kerberos, DNS, and certificate management into one integrated identity domain.

**Links:** [GitHub](https://github.com/freeipa/freeipa) · [Docs](https://www.freeipa.org/page/Documentation)

## Overview

FreeIPA is effectively "Active Directory for Linux" — centralized user/group management, Kerberos authentication, and DNS, all integrated. Useful for practicing enterprise-style Linux identity management, or centralizing auth across a homelab's Linux boxes.

## Install / Deploy

```bash
sudo dnf install freeipa-server
sudo ipa-server-install
```

## Common Commands

```bash
ipa user-add jdoe --first=John --last=Doe
ipa group-add admins
kinit admin
```

## Lab Exercise

Deploy FreeIPA as your lab's central identity domain, join a couple of lab Linux VMs to it (`ipa-client-install`), and confirm you can log into either VM with a centrally-managed FreeIPA user account.

## Related Tools

- [Keycloak](keycloak.md) · [Authentik](authentik.md) — complementary web-app SSO layer on top
