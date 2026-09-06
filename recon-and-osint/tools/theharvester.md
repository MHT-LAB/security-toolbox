# theHarvester

Pulls emails, subdomains, and names from public sources (search engines, PGP key servers, certificate transparency logs).

**Links:** [GitHub](https://github.com/laramies/theHarvester) · [Docs](https://github.com/laramies/theHarvester/wiki)

## Overview

theHarvester is a good first-pass tool for gathering the "who and what" of an organization from open sources before deeper enumeration — email addresses in particular are useful for phishing-awareness testing and password-spray target lists.

## Install / Deploy

```bash
# Kali: preinstalled. Elsewhere:
git clone https://github.com/laramies/theHarvester.git
cd theHarvester && pip install -r requirements.txt
```

## Common Commands

```bash
theHarvester -d example.com -b all
theHarvester -d example.com -b crtsh,bing -l 500
```

## Lab Exercise

Run theHarvester against a domain you control, and cross-reference the emails found against what [Sherlock](sherlock.md) or [Holehe](holehe.md) can tell you about those addresses elsewhere.

## Related Tools

- [Sherlock](sherlock.md) · [Holehe](holehe.md) — pivot from an email/username found here
- [OWASP Amass](owasp-amass.md) — broader subdomain-focused alternative
