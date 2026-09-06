# DevSec Hardening Framework (Ansible)

Ansible playbooks that codify OS/SSH/nginx hardening baselines — apply CIS-style hardening as infrastructure-as-code instead of manual checklist work.

**Links:** [GitHub](https://github.com/dev-sec/ansible-collection-hardening) · [Docs](https://dev-sec.io)

## Overview

The DevSec project maintains Ansible (and Chef/Puppet) hardening collections for Linux, SSH, nginx, MySQL, and more — apply once to bake in baseline hardening, and re-run on a schedule to correct drift automatically rather than relying on a one-time manual audit.

## Install / Deploy

```bash
ansible-galaxy collection install devsec.hardening
```

## Common Commands

```yaml
# playbook.yml
- hosts: all
  collections:
    - devsec.hardening
  roles:
    - os_hardening
    - ssh_hardening
```
```bash
ansible-playbook -i inventory playbook.yml
```

## Lab Exercise

Apply the `ssh_hardening` role to a lab VM, then confirm with [Lynis](lynis.md) or manual inspection that the SSH configuration now matches CIS-style baselines (no root login, strong ciphers only, etc.).

## Related Tools

- [Lynis](lynis.md) — verify the hardening this applies
- [Chef InSpec](chef-inspec.md) — compliance-verification counterpart from the same project family
