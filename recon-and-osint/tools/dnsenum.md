# dnsenum

Classic Perl-based DNS recon tool — brute-force subdomain enumeration, zone transfers, and Google scraping for additional names.

**Links:** [GitHub](https://github.com/fwaeytens/dnsenum)

## Overview

Older than dnsrecon but still shipped in Kali and still useful as a second opinion — dnsenum's brute-force wordlist approach sometimes finds names other tools' passive sources miss.

## Install / Deploy

```bash
sudo apt install dnsenum
```

## Common Commands

```bash
dnsenum example.com
dnsenum --dnsserver 8.8.8.8 -f subdomains.txt example.com
```

## Lab Exercise

Run dnsenum with a wordlist against a lab domain, and compare its brute-force hits against [dnsrecon](dnsrecon.md)'s passive-plus-brute output on the same domain.

## Related Tools

- [dnsrecon](dnsrecon.md) — modern alternative with broader feature coverage
