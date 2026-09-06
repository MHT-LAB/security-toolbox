# Sublist3r

Subdomain enumeration using search engines and OSINT sources — an older, simpler, still-useful tool for a quick subdomain list.

**Links:** [GitHub](https://github.com/aboul3la/Sublist3r)

## Overview

Sublist3r queries search engines (Google, Bing, Yahoo), Netcraft, VirusTotal, and a few other sources to build a subdomain list quickly. It's less thorough than Amass or Subfinder but fast and dependency-light, making it a reasonable first check.

## Install / Deploy

```bash
git clone https://github.com/aboul3la/Sublist3r.git
cd Sublist3r && pip install -r requirements.txt
```

## Common Commands

```bash
python3 sublist3r.py -d example.com
python3 sublist3r.py -d example.com -o subs.txt -v
```

## Lab Exercise

Run Sublist3r against a domain you own alongside [Subfinder](subfinder.md), and compare result counts/overlap — a good exercise for understanding why most working recon setups run more than one subdomain tool.

## Related Tools

- [Subfinder](subfinder.md) · [OWASP Amass](owasp-amass.md) — more actively maintained alternatives
