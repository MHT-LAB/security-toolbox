# TruffleHog

Deep secret-scanning across repos and live credentials verification — beyond pattern matching, it actually tests whether a found credential is still live/valid.

**Links:** [GitHub](https://github.com/trufflesecurity/trufflehog) · [Docs](https://github.com/trufflesecurity/trufflehog#trufflehog)

## Overview

TruffleHog scans git history, filesystems, and even live services (Slack, S3 buckets) for secrets, and for many credential types can verify whether the found secret is still active — cutting through "is this a real finding or an old rotated key" ambiguity automatically.

## Install / Deploy

```bash
brew install trufflehog
# or: docker run trufflesecurity/trufflehog:latest
```

## Common Commands

```bash
trufflehog git file://./my-repo
trufflehog filesystem ./my-project --only-verified
```

## Lab Exercise

Run TruffleHog with `--only-verified` against a repo you maintain, so you only see credentials it confirmed are still live — a much lower-noise result than Gitleaks' pure pattern-match approach.

## Related Tools

- [Gitleaks](gitleaks.md) — faster, pattern-match-only alternative
