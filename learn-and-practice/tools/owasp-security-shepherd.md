# OWASP Security Shepherd

Web/mobile app security training platform with progressive challenges — OWASP's own structured training tool, similar goal to WebGoat but with a broader challenge library and scoring.

**Links:** [GitHub](https://github.com/OWASP/SecurityShepherd)

## Overview

Security Shepherd covers OWASP Top 10-style vulnerabilities across web and mobile, with a points/leaderboard structure that suits classroom or team-based training settings, not just solo practice.

## Install / Deploy

```bash
git clone https://github.com/OWASP/SecurityShepherd.git
cd SecurityShepherd && docker-compose up -d
```

## Common Commands

Web-UI driven challenge platform; no special CLI beyond the tools you use to solve each challenge (Burp Suite, sqlmap, etc.).

## Lab Exercise

Deploy Security Shepherd for a small group (or solo), and use it as a structured follow-up after [DVWA](../../test-and-exploit/tools/dvwa.md)/[WebGoat](../../test-and-exploit/tools/webgoat.md) once you want scored, competitive-style practice.

## Related Tools

- [DVWA](../../test-and-exploit/tools/dvwa.md) · [WebGoat](../../test-and-exploit/tools/webgoat.md) · [Juice Shop](../../test-and-exploit/tools/juice-shop.md) — comparable self-hosted training targets
