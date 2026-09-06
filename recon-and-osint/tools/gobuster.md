# Gobuster

Directory/file/DNS/vhost brute-forcer written in Go — fast wordlist-based discovery of hidden endpoints and subdomains.

**Links:** [GitHub](https://github.com/OJ/gobuster) · [Docs](https://github.com/OJ/gobuster#usage)

## Overview

Gobuster brute-forces four different modes: `dir` (web paths), `dns` (subdomains), `vhost` (virtual hosts sharing an IP), and `s3`/`gcs` (cloud storage buckets). Its Go concurrency makes it noticeably faster than older Python equivalents like DIRB.

## Install / Deploy

```bash
sudo apt install gobuster
# or: go install github.com/OJ/gobuster/v3@latest
```

## Common Commands

```bash
gobuster dir -u http://target -w /usr/share/wordlists/dirb/common.txt
gobuster dns -d example.com -w subdomains.txt
gobuster vhost -u http://target -w vhosts.txt
```

## Lab Exercise

Run `gobuster dir` against [DVWA](../../test-and-exploit/tools/dvwa.md) or [Juice Shop](../../test-and-exploit/tools/juice-shop.md) with a common wordlist to find hidden admin/debug paths, then manually verify each hit in a browser.

## Related Tools

- [ffuf](ffuf.md) — faster, more flexible fuzzing alternative
- [Nikto](../../test-and-exploit/tools/nikto.md) — complementary misconfiguration scan
