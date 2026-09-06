# bWAPP

"Buggy web application" covering 100+ vulnerability classes — an older but very broad-coverage alternative to DVWA, useful when you want more variety of vulnerability types in one target.

**Links:** [GitHub](https://github.com/ismailtasdelen/bWAPP)

## Overview

bWAPP predates Juice Shop as a broad-vulnerability-coverage target, with over 100 distinct bug types across web, mobile-adjacent, and even some SOAP/AJAX-specific issues — a reasonable choice specifically when you want to practice a vulnerability class DVWA/Juice Shop don't cover.

## Install / Deploy

```bash
git clone https://github.com/ismailtasdelen/bWAPP.git
# Deploy on a LAMP stack, or use the pre-built bee-box VM referenced in the repo
```

## Common Commands

Standard web-app testing workflow with [Burp Suite](../../test-and-exploit/tools/burp-suite.md)/[sqlmap](../../test-and-exploit/tools/sqlmap.md) depending on the specific bug being practiced.

## Lab Exercise

Pick a vulnerability class not covered by [DVWA](../../test-and-exploit/tools/dvwa.md)/[Juice Shop](../../test-and-exploit/tools/juice-shop.md) (e.g. a specific SOAP or AJAX bug) and practice it specifically in bWAPP.

## Related Tools

- [DVWA](../../test-and-exploit/tools/dvwa.md) · [Juice Shop](../../test-and-exploit/tools/juice-shop.md) — comparable but narrower-coverage targets
