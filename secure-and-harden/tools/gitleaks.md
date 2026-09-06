# Gitleaks

Scans git repos/history for hardcoded secrets before they leak — checks not just the current commit but full history, since a secret removed later is still exposed in old commits.

**Links:** [GitHub](https://github.com/gitleaks/gitleaks) · [Docs](https://github.com/gitleaks/gitleaks#usage)

## Overview

Gitleaks pattern-matches for API keys, tokens, and credentials across a repository's entire commit history, not just the working tree — a secret committed and later deleted is still findable in git history unless the history itself is rewritten.

## Install / Deploy

```bash
brew install gitleaks
# or: go install github.com/gitleaks/gitleaks/v8@latest
```

## Common Commands

```bash
gitleaks detect --source . -v
gitleaks protect --staged   # pre-commit check on staged changes only
```

## Lab Exercise

Run Gitleaks against a repo you maintain (including full history with `detect`), and if it finds anything, treat the exposed secret as compromised — rotate it, don't just delete the commit.

## Related Tools

- [TruffleHog](trufflehog.md) — deeper verification-focused alternative
