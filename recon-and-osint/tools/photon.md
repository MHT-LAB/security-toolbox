# Photon

Fast crawler for extracting URLs, endpoints, and secrets from a site — walks a target and pulls out everything from JS files, forms, and comments that looks like a lead.

**Links:** [GitHub](https://github.com/s0md3v/Photon)

## Overview

Photon crawls a target site and extracts structured leads: URLs, emails, social media links, files, JS endpoints, and secrets accidentally left in source (API keys, etc.) — a good pre-step before manual testing.

## Install / Deploy

```bash
git clone https://github.com/s0md3v/Photon.git
cd Photon && pip install -r requirements.txt
```

## Common Commands

```bash
python3 photon.py -u http://target --level 3
python3 photon.py -u http://target -o output_dir --keys   # extract secrets/API keys
```

## Lab Exercise

Crawl [Juice Shop](../../test-and-exploit/tools/juice-shop.md) with Photon and check the extracted endpoint list against what you find manually in [Burp Suite](../../test-and-exploit/tools/burp-suite.md)'s HTTP history after browsing the app normally.

## Related Tools

- [Burp Suite](../../test-and-exploit/tools/burp-suite.md) — manual verification of what Photon finds
