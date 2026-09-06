# Security Toolbox

A curated, categorized list of free and open-source cybersecurity tools and reference sites — recon, detection, forensics, offensive testing, hardening, homelab/networking, and hands-on learning.

Organized by what the tool *does*, not by product category. Pick the folder for the job, not the vendor.

## Categories

- [`recon-and-osint/`](recon-and-osint/README.md) — find and map what's out there
- [`detect-and-respond/`](detect-and-respond/README.md) — monitor, alert, and investigate
- [`analyze-and-investigate/`](analyze-and-investigate/README.md) — forensics and malware analysis
- [`test-and-exploit/`](test-and-exploit/README.md) — offensive testing and validation
- [`secure-and-harden/`](secure-and-harden/README.md) — audit and lock down configurations
- [`network-and-homelab/`](network-and-homelab/README.md) — self-hosted infrastructure and networking
- [`learn-and-practice/`](learn-and-practice/README.md) — hands-on ranges, CTFs, and training
- [`threat-intel-and-reference/`](threat-intel-and-reference/README.md) — ISACs, sharing communities, standards bodies, and vendor intel feeds

**Every category is broken out into per-tool pages** under `<category>/tools/` — each tool gets its own file with Overview, Install/Deploy, Common Commands, a concrete Lab Exercise, and Related Tools, instead of a one-line link. Each category `README.md` is an index table (Top 15 + "more tools worth knowing," plus a Deception & Honeypots section under `detect-and-respond/`) pointing to every page. Links point to the tool's GitHub repo where one exists; commercial/SaaS tools with no public repo (Burp Suite, Shodan, Maltego, TryHackMe, HTB, Proxmox, CISA/vendor threat-intel portals) link to the official site instead and say so. Where the same tool is genuinely shared across categories (MISP, OPNsense, Metasploitable3/DVWA/WebGoat/Juice Shop), only one category owns the page — the others cross-reference it rather than duplicating content.

240 markdown files, 231 tool pages across 8 categories — every internal link has been verified to resolve.

## Entry format

Each category README is a table linking to `tools/<tool-slug>.md`. Every tool page follows:

    # Tool Name
    One-line description.
    **Links:** [GitHub](...) · [Docs](...)
    ## Overview
    ## Install / Deploy
    ## Common Commands
    ## Lab Exercise
    ## Related Tools

For `threat-intel-and-reference/`, where most entries are communities or reference sites rather than software, "Install/Deploy" and "Common Commands" become "how to access/join" and "how to query the feed."

## Contributing

Suggestions welcome — open an issue or a PR using the entry format above.
