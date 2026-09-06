# Semaphore UI

Web UI for running and scheduling Ansible playbooks — turns ad-hoc `ansible-playbook` runs into a scheduled, auditable, team-shareable workflow.

**Links:** [GitHub](https://github.com/semaphoreui/semaphore) · [Docs](https://docs.semaphoreui.com)

## Overview

Semaphore gives Ansible a web front end — store playbooks, define inventories, and run/schedule jobs with a visible history of what ran, when, and with what result, instead of everyone running playbooks from their own laptop.

## Install / Deploy

```bash
docker run -d -p 3000:3000 -e SEMAPHORE_DB_DIALECT=bolt semaphoreui/semaphore:latest
```

## Common Commands

Web-UI driven; connect a git repo containing playbooks, define an inventory, and run/schedule tasks through the dashboard.

## Lab Exercise

Connect Semaphore to a git repo containing the [DevSec Hardening](../../secure-and-harden/tools/devsec-hardening.md) Ansible roles, and run them against a lab inventory through Semaphore instead of the raw CLI — then schedule a recurring run to catch configuration drift.

## Related Tools

- [DevSec Hardening Framework](../../secure-and-harden/tools/devsec-hardening.md) — a good first playbook to run through it
- [Cockpit](cockpit.md) — complementary single-server admin UI
