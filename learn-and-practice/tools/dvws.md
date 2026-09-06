# Damn Vulnerable Web Services (DVWS)

Vulnerable SOAP/REST API target for web-service security testing — fills the API-specific gap that DVWA/Juice Shop's traditional web-app focus doesn't fully cover.

**Links:** [GitHub](https://github.com/snoopysecurity/dvws)

## Overview

Most beginner-friendly vulnerable apps focus on traditional web pages; DVWS specifically targets SOAP and REST API vulnerabilities (XXE, insecure deserialization in API contexts) — useful once you're specifically practicing API security rather than classic web-app flaws.

## Install / Deploy

```bash
git clone https://github.com/snoopysecurity/dvws.git
# Follow repo's setup instructions (LAMP-stack based)
```

## Common Commands

Use [Burp Suite](../../test-and-exploit/tools/burp-suite.md)'s Repeater against SOAP/REST endpoints; standard API testing workflow.

## Lab Exercise

Deploy DVWS and use Burp Suite to intercept and manipulate a SOAP request, testing specifically for XXE — a good complement to the more general web-app work done against [Juice Shop](../../test-and-exploit/tools/juice-shop.md).

## Related Tools

- [Burp Suite](../../test-and-exploit/tools/burp-suite.md) — primary tool for API testing
