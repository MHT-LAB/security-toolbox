# Semgrep

Static analysis (SAST) for finding security bugs in source code before it ships — pattern-based rules across dozens of languages, fast enough for CI on every commit.

**Links:** [GitHub](https://github.com/semgrep/semgrep) · [Docs](https://semgrep.dev/docs/)

## Overview

Semgrep matches code patterns (not just regex — it understands syntax trees) against a huge community-maintained ruleset (`p/security-audit`, `p/owasp-top-ten`, and more), catching issues like hardcoded secrets, SQL injection patterns, and insecure deserialization directly in source code.

## Install / Deploy

```bash
pip install semgrep
```

## Common Commands

```bash
semgrep --config p/security-audit .
semgrep --config p/owasp-top-ten .
```

## Lab Exercise

Run `semgrep --config p/security-audit` against a small vulnerable codebase (e.g. [Juice Shop](../../test-and-exploit/tools/juice-shop.md)'s source, which is open source) and review how many of its intentional vulnerabilities Semgrep's static rules actually catch versus what only shows up at runtime.

## Related Tools

- [Bandit](bandit.md) — narrower, Python-specific SAST alternative
- [Gitleaks](gitleaks.md) · [TruffleHog](trufflehog.md) — complementary secret-scanning
