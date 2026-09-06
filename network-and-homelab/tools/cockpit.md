# Cockpit

Web-based admin console for managing Linux servers — a browser-based alternative to raw SSH for common sysadmin tasks (storage, services, logs, updates).

**Links:** [GitHub](https://github.com/cockpit-project/cockpit) · [Docs](https://cockpit-project.org/documentation.html)

## Overview

Cockpit provides a lightweight web UI directly on a Linux server for viewing logs, managing systemd services, configuring storage/networking, and applying updates — useful for quick admin tasks without opening a terminal, especially for less CLI-comfortable team members.

## Install / Deploy

```bash
sudo apt install cockpit
sudo systemctl enable --now cockpit.socket
```

## Common Commands

Web-UI driven at `https://<server-ip>:9090`; no CLI needed for basic use.

## Lab Exercise

Enable Cockpit on a lab server, use it to view a systemd service's logs and restart it through the browser, then confirm the same action via SSH/systemctl to understand what Cockpit is doing underneath.

## Related Tools

- [Semaphore UI](semaphore-ui.md) — complementary for managing multiple servers via Ansible instead of one at a time
