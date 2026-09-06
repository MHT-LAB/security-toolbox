# Recon-ng

Modular web reconnaissance framework, built like Metasploit — modules for each OSINT source, a shared workspace, and reporting.

**Links:** [GitHub](https://github.com/lanmaster53/recon-ng) · [Docs](https://github.com/lanmaster53/recon-ng/wiki)

## Overview

Recon-ng gives OSINT gathering the same console-and-module structure Metasploit gives exploitation — `marketplace install` pulls in modules, `workspaces` isolate engagements, and results feed a shared database you can query and report from.

## Install / Deploy

```bash
git clone https://github.com/lanmaster53/recon-ng.git
cd recon-ng && pip install -r REQUIREMENTS
./recon-ng
```

## Common Commands

```text
workspaces create example
marketplace install all
modules load recon/domains-hosts/hackertarget
options set SOURCE example.com
run
```

## Lab Exercise

Create a workspace for a domain you control, install the `hackertarget` and `certificate transparency` modules, run them, and query the resulting hosts table — compare the coverage against [OWASP Amass](owasp-amass.md) on the same domain.

## Related Tools

- [OWASP Amass](owasp-amass.md) · [SpiderFoot](spiderfoot.md) — similar all-in-one OSINT frameworks
