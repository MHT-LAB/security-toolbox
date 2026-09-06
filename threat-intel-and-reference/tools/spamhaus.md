# Spamhaus

Free DNSBL/blocklists for spam, malware, and botnet C2 infrastructure — widely used by mail servers and firewalls as an authoritative reputation source.

**Links:** [Official site](https://www.spamhaus.org)

## Overview

Spamhaus maintains some of the most widely-trusted DNS-based blocklists in existence (SBL, XBL, PBL) — most mail servers and many firewalls query Spamhaus lists directly as part of standard spam/malware filtering, making it a foundational rather than optional reference.

## Install / Deploy

```text
Most mail server software (Postfix, Exim) has built-in support for querying
Spamhaus DNSBLs — enable via the mail server's own RBL/DNSBL configuration.
```

## Common Commands

```bash
dig +short 4.3.2.1.zen.spamhaus.org   # manual DNSBL lookup for IP 1.2.3.4
```

## Lab Exercise

Configure your lab mail server (if you run one) to query Spamhaus's ZEN blocklist, and manually check a known-spam-source IP against it with `dig` to confirm the lookup format.

## Related Tools

- [abuse.ch](abusech.md) — comparable free malware/botnet tracking feeds
