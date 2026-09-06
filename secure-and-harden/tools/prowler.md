# Prowler

AWS/Azure/GCP security best-practices and compliance auditing — checks cloud account configuration against CIS benchmarks and other frameworks.

**Links:** [GitHub](https://github.com/prowler-cloud/prowler) · [Docs](https://docs.prowler.cloud)

## Overview

Prowler runs hundreds of checks against a cloud account's actual configuration — public S3 buckets, overly permissive IAM policies, unencrypted resources — mapped to CIS and other compliance frameworks, producing a scored report per account.

## Install / Deploy

```bash
pip install prowler
prowler aws   # requires AWS credentials configured
```

## Common Commands

```bash
prowler aws --compliance cis_2.0_aws
prowler azure
prowler gcp
```

## Lab Exercise

Run Prowler against a personal/lab AWS account (never a client's without authorization), review the findings, fix the highest-severity one (commonly an overly permissive S3 bucket policy), and re-scan to confirm.

## Related Tools

- [ScoutSuite](scoutsuite.md) — comparable multi-cloud alternative
