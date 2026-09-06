# ffuf

Fast web fuzzer for endpoints, parameters, and vhosts — arguably the most flexible fuzzing tool on this list, since almost any part of a request can be the `FUZZ` keyword.

**Links:** [GitHub](https://github.com/ffuf/ffuf) · [Docs](https://github.com/ffuf/ffuf#example-usage)

## Overview

Where Gobuster is mode-restricted, ffuf lets you put the `FUZZ` placeholder anywhere in a request — the URL path, a query parameter, a header, even POST body — making it useful well beyond simple directory brute-forcing (parameter discovery, auth bypass testing, etc.).

## Install / Deploy

```bash
go install github.com/ffuf/ffuf/v2@latest
```

## Common Commands

```bash
ffuf -u http://target/FUZZ -w wordlist.txt
ffuf -u http://target/api?FUZZ=1 -w params.txt -fc 404
ffuf -u http://target/ -H "X-Custom-Header: FUZZ" -w wordlist.txt
```

## Lab Exercise

Against [Juice Shop](../../test-and-exploit/tools/juice-shop.md), fuzz for hidden API endpoints under `/api/FUZZ` using a common API-path wordlist, filtering out 404 responses with `-fc 404` to cut noise.

## Related Tools

- [Gobuster](gobuster.md) — simpler, mode-based alternative
- [Burp Suite](../../test-and-exploit/tools/burp-suite.md) — capture requests to fuzz with `-request`
