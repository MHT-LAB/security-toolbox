# Recon & OSINT

Finding and mapping what's publicly visible — before anyone else does.

Every tool below has its own page under [`tools/`](tools/) with Overview, Install/Deploy, Common Commands, a concrete Lab Exercise, and Related Tools — not just a link out.

## 🏆 Top 15 (most widely used)

| Tool | What it does |
|---|---|
| [Nmap](tools/nmap.md) | The standard for network discovery and port scanning. |
| [Masscan](tools/masscan.md) | Internet-scale port scanner, far faster than Nmap for broad sweeps. |
| [OWASP Amass](tools/owasp-amass.md) | Attack surface mapping and subdomain enumeration. |
| [Subfinder](tools/subfinder.md) | Fast passive subdomain discovery from ProjectDiscovery. |
| [theHarvester](tools/theharvester.md) | Pulls emails, subdomains, and names from public sources. |
| [Recon-ng](tools/recon-ng.md) | Modular web reconnaissance framework, built like Metasploit. |
| [SpiderFoot](tools/spiderfoot.md) | Automates OSINT collection across 200+ data sources. |
| [Nuclei](tools/nuclei.md) | Template-driven scanner for known misconfigurations and CVEs. |
| [httpx](tools/httpx.md) | Fast HTTP probing/toolkit for live-host discovery. |
| [Shodan](tools/shodan.md) | Search engine for internet-connected devices (SaaS, free tier). |
| [Maltego Community Edition](tools/maltego-ce.md) | Link-analysis tool for mapping entity relationships (commercial). |
| [Sublist3r](tools/sublist3r.md) | Subdomain enumeration using search engines and OSINT sources. |
| [Gobuster](tools/gobuster.md) | Directory/file/DNS/vhost brute-forcer written in Go. |
| [ffuf](tools/ffuf.md) | Fast web fuzzer for endpoints, parameters, and vhosts. |
| [WhatWeb](tools/whatweb.md) | Web technology fingerprinting. |

## More tools worth knowing

| Tool | What it does |
|---|---|
| [dnsx](tools/dnsx.md) | Fast, multi-purpose DNS toolkit for bulk resolution. |
| [dnsrecon](tools/dnsrecon.md) | DNS enumeration and zone-transfer testing. |
| [dnsenum](tools/dnsenum.md) | Classic Perl-based DNS recon tool. |
| [Photon](tools/photon.md) | Fast crawler for extracting URLs, endpoints, and secrets from a site. |
| [Sherlock](tools/sherlock.md) | Finds usernames across social media platforms. |
| [GHunt](tools/ghunt.md) | Investigates Google accounts via public data. |
| [Holehe](tools/holehe.md) | Checks whether an email is registered on other sites. |
| [Metagoofil](tools/metagoofil.md) | Extracts metadata from public documents. |
| [Osmedeus](tools/osmedeus.md) | Automated recon pipeline for continuous attack-surface monitoring. |
| [gau (GetAllUrls)](tools/gau.md) | Fetches known URLs from Wayback Machine, Common Crawl, and OTX. |
| [waybackurls](tools/waybackurls.md) | Pulls historical URLs for a domain from the Wayback Machine. |
| [assetfinder](tools/assetfinder.md) | Finds related domains and subdomains. |
| [Aquatone](tools/aquatone.md) | Visual inventory of websites via screenshots across many hosts. |
| [EyeWitness](tools/eyewitness.md) | Screenshots websites and reports server info/default creds. |
| [Fierce](tools/fierce.md) | DNS reconnaissance for locating non-contiguous IP space. |
| [dnstwist](tools/dnstwist.md) | Detects typosquatting and phishing domains that mimic yours. |
| [OSINT Framework](tools/osint-framework.md) | Curated index of OSINT resources by category. |
| [IVRE](tools/ivre.md) | Network recon framework for internal asset tracking. |
| [Sn1per](tools/sn1per.md) | Automated pentest recon scanner chaining many of the above. |
| [AbuseIPDB](tools/abuseipdb.md) | Free crowdsourced IP-address reputation lookup. |

*General infrastructure guidance:* run recon tooling from a dedicated, isolated jump host (not your daily driver), keep results in a scoped case-management tool (see [`detect-and-respond/`](../detect-and-respond/README.md) — TheHive) rather than loose files, and never point active scanners ([Nmap](tools/nmap.md), [Masscan](tools/masscan.md), [Nuclei](tools/nuclei.md), [ffuf](tools/ffuf.md)) at anything outside written authorization.
