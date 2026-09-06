# MxToolbox Email Header Analyzer

Free RFC822 email-header parser for tracing a phishing email's real origin — decodes routing hops, SPF/DKIM/DMARC results, and originating IP from a raw header.

**Links:** [Official site](https://mxtoolbox.com/EmailHeaders.aspx) — SaaS, no public repo.

## Overview

A phishing email's raw header contains the actual sending infrastructure (originating IP, relay hops, authentication results) that the friendly "From" display name hides. This tool parses that raw header into a readable breakdown without needing to read RFC822 format by hand.

## Install / Deploy

```text
No installation — paste a raw email header (View Source / Show Original in your mail client) into the web form.
```

## Common Commands

Not applicable — web form only; paste the full raw header text.

## Lab Exercise

Take a real (or simulated, from [Gophish](../../test-and-exploit/tools/gophish.md)) phishing email's raw header, paste it in, and confirm you can identify the originating IP and whether SPF/DKIM/DMARC passed — then check that originating IP against [AbuseIPDB](../../recon-and-osint/tools/abuseipdb.md).

## Related Tools

- [Gophish](../../test-and-exploit/tools/gophish.md) — generates the kind of email this analyzes
- [AbuseIPDB](../../recon-and-osint/tools/abuseipdb.md) — next step on the originating IP
