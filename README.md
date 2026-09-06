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

Each category README leads with a **🏆 Top 15** — the most widely adopted tools for that job, by real-world usage — followed by a longer **More tools worth knowing** list. Links point to the tool's GitHub repo where one exists; commercial/SaaS tools with no public repo (Burp Suite, Shodan, Maltego, TryHackMe, HTB, Proxmox) link to the official site instead and say so.

**[`test-and-exploit/`](test-and-exploit/README.md) is fully broken out into per-tool pages** under [`test-and-exploit/tools/`](test-and-exploit/tools/) — each tool gets its own file with Overview, Install/Deploy, Common Commands, a concrete Lab Exercise, and Related Tools, instead of a one-line link. The category README is now an index table pointing to each page. This is the pattern the other categories will get next, once it's confirmed useful in this one.

## Entry format

**Index-style categories** (currently `test-and-exploit/`): the README is a table linking to `tools/<tool-slug>.md`. Each tool page follows:

    # Tool Name
    One-line description.
    **Links:** [GitHub](...) · [Docs](...)
    ## Overview
    ## Install / Deploy
    ## Common Commands
    ## Lab Exercise
    ## Related Tools

**Flat-list categories** (everything else, for now):

    - [Tool Name](https://github-link-or-site) — what it does, one line.
      *Use it:* the most appropriate way to test or run this in a real lab/infrastructure — not just what it is, but how to actually deploy or invoke it safely.

## Contributing

Suggestions welcome — open an issue or a PR using the entry format above.
