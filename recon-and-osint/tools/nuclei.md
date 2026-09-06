# Nuclei

Template-driven scanner for known misconfigurations and CVEs — community-maintained YAML templates mean new checks ship fast after a CVE drops.

**Links:** [GitHub](https://github.com/projectdiscovery/nuclei) · [Docs](https://docs.projectdiscovery.io/tools/nuclei)

## Overview

Nuclei runs a huge, community-maintained library of YAML-defined checks against a target — CVEs, exposed panels, default credentials, misconfigurations. Because templates are just YAML, new checks appear within hours of a public disclosure, which is both its strength and why it's noisy against anything not fully patched.

## Install / Deploy

```bash
go install -v github.com/projectdiscovery/nuclei/v3/cmd/nuclei@latest
nuclei -update-templates
```

## Common Commands

```bash
nuclei -u https://target -t cves/
nuclei -l urls.txt -t exposed-panels/
nuclei -u https://target -severity critical,high
```

## Lab Exercise

Run `nuclei -t cves/` against [Metasploitable3](../../test-and-exploit/tools/metasploitable3.md) or [Juice Shop](../../test-and-exploit/tools/juice-shop.md) and compare the findings to what [Nikto](../../test-and-exploit/tools/nikto.md) reports on the same target.

## Related Tools

- [httpx](httpx.md) — typical pipeline partner (`subfinder | httpx | nuclei`)
- [Nikto](../../test-and-exploit/tools/nikto.md) — narrower, server-focused alternative
