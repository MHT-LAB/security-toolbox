# WhatWeb

Web technology fingerprinting — identifies CMS, frameworks, JavaScript libraries, server software, and analytics tools running behind a URL.

**Links:** [GitHub](https://github.com/urbanadventurer/WhatWeb)

## Overview

WhatWeb runs 1,800+ fingerprint plugins against a target, returning a compact summary of what's running (WordPress version, Apache version, jQuery version, etc.) — useful groundwork before searching [Exploit Database](../../test-and-exploit/tools/exploit-database.md) for version-specific issues.

## Install / Deploy

```bash
sudo apt install whatweb
```

## Common Commands

```bash
whatweb target.com
whatweb -v target.com          # verbose, show plugin detail
whatweb --aggression 3 target.com   # more aggressive fingerprinting
```

## Lab Exercise

Run WhatWeb against [Metasploitable3](../../test-and-exploit/tools/metasploitable3.md), note the identified software/versions, and search [Exploit Database](../../test-and-exploit/tools/exploit-database.md) for each to see which have known public PoCs.

## Related Tools

- [Nikto](../../test-and-exploit/tools/nikto.md) — complementary misconfiguration-focused scan
- [Exploit Database](../../test-and-exploit/tools/exploit-database.md) — next step once you know exact versions
