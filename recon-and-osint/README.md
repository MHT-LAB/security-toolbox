# Recon & OSINT

Finding and mapping what's publicly visible — before anyone else does.

## 🏆 Top 15 (most widely used)

- **[Nmap](https://github.com/nmap/nmap)** — the standard for network discovery and port scanning.
  *Use it:* run against your own lab subnet (`nmap -sV -sC target`) before ever pointing it at anything you don't own; most MSPs run it from a jump box for authorized client scans.
- **[Masscan](https://github.com/robertdavidgraham/masscan)** — internet-scale port scanner, orders of magnitude faster than Nmap for broad sweeps.
- **[OWASP Amass](https://github.com/owasp-amass/amass)** — attack surface mapping and subdomain enumeration.
- **[Subfinder](https://github.com/projectdiscovery/subfinder)** — fast passive subdomain discovery from ProjectDiscovery.
- **[theHarvester](https://github.com/laramies/theHarvester)** — pulls emails, subdomains, and names from public sources.
- **[Recon-ng](https://github.com/lanmaster53/recon-ng)** — modular web reconnaissance framework, built like Metasploit.
- **[SpiderFoot](https://github.com/smicallef/spiderfoot)** — automates OSINT collection across 200+ data sources; run the web UI in a container for a standing recon dashboard.
- **[Nuclei](https://github.com/projectdiscovery/nuclei)** — template-driven scanner for known misconfigurations and CVEs.
- **[httpx](https://github.com/projectdiscovery/httpx)** — fast HTTP probing/toolkit for live-host discovery.
- **[Shodan](https://www.shodan.io) ([python CLI](https://github.com/achillean/shodan-python))** — search engine for internet-connected devices; SaaS, free tier covers most lookups.
  *Use it:* query your own public IP ranges periodically to see what an attacker sees exposed — this is passive, no scanning traffic touches your assets.
- **[Maltego Community Edition](https://www.maltego.com/community-edition/)** — link-analysis tool for mapping entity relationships; commercial, free CE tier, no public core repo.
- **[Sublist3r](https://github.com/aboul3la/Sublist3r)** — subdomain enumeration using search engines and OSINT sources.
- **[Gobuster](https://github.com/OJ/gobuster)** — directory/file/DNS/vhost brute-forcer written in Go.
- **[ffuf](https://github.com/ffuf/ffuf)** — fast web fuzzer for endpoints, parameters, and vhosts.
- **[WhatWeb](https://github.com/urbanadventurer/WhatWeb)** — web technology fingerprinting.

## More tools worth knowing

- **[dnsx](https://github.com/projectdiscovery/dnsx)** — fast, multi-purpose DNS toolkit for bulk resolution.
- **[dnsrecon](https://github.com/darkoperator/dnsrecon)** — DNS enumeration and zone-transfer testing.
- **[dnsenum](https://github.com/fwaeytens/dnsenum)** — classic Perl-based DNS recon tool.
- **[Photon](https://github.com/s0md3v/Photon)** — fast crawler for extracting URLs, endpoints, and secrets from a site.
- **[Sherlock](https://github.com/sherlock-project/sherlock)** — finds usernames across social media platforms.
- **[GHunt](https://github.com/mxrch/GHunt)** — investigates Google accounts via public data (email, calendar, maps).
- **[Holehe](https://github.com/megadose/holehe)** — checks whether an email is registered on other sites.
- **[Metagoofil](https://github.com/opsdisk/metagoofil)** — extracts metadata from public documents (PDF, DOCX, etc.).
- **[Osmedeus](https://github.com/j3ssie/osmedeus)** — automated recon pipeline/framework for continuous attack-surface monitoring.
- **[gau (GetAllUrls)](https://github.com/lc/gau)** — fetches known URLs from Wayback Machine, Common Crawl, and OTX.
- **[waybackurls](https://github.com/tomnomnom/waybackurls)** — pulls historical URLs for a domain from the Wayback Machine.
- **[assetfinder](https://github.com/tomnomnom/assetfinder)** — finds related domains and subdomains.
- **[Aquatone](https://github.com/michenriksen/aquatone)** — visual inventory of websites via screenshots across many hosts.
- **[EyeWitness](https://github.com/FortyNorthSecurity/EyeWitness)** — screenshots websites and reports server info/default creds.
- **[Fierce](https://github.com/mschwager/fierce)** — DNS reconnaissance for locating non-contiguous IP space.
- **[dnstwist](https://github.com/elceef/dnstwist)** — detects typosquatting and phishing domains that mimic yours.
- **[OSINT Framework](https://github.com/lockfale/OSINT-Framework)** — curated index of OSINT resources by category (site + repo).
- **[IVRE](https://github.com/ivre/ivre)** — network recon framework built on Nmap/Masscan/Zeek data for internal asset tracking.
- **[Sn1per](https://github.com/1N3/Sn1per)** — automated pentest recon scanner that chains many of the above tools.
- **[AbuseIPDB](https://www.abuseipdb.com)** — free crowdsourced IP-address reputation and abuse-report lookup; SaaS, no public repo.

*General infrastructure guidance:* run recon tooling from a dedicated, isolated jump host (not your daily driver), keep results in a scoped case-management tool (see [`detect-and-respond/`](../detect-and-respond/README.md) — TheHive) rather than loose files, and never point active scanners (Nmap, Masscan, Nuclei, ffuf) at anything outside written authorization.
