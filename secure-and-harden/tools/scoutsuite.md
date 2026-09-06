# ScoutSuite

Multi-cloud security-posture auditing tool — generates a browsable HTML report of a cloud account's configuration issues across AWS, Azure, and GCP.

**Links:** [GitHub](https://github.com/nccgroup/ScoutSuite) · [Docs](https://github.com/nccgroup/ScoutSuite/wiki)

## Overview

ScoutSuite's output is a static, browsable HTML report rather than Prowler's compliance-framework-mapped CLI output — useful when you want a shareable report for a non-technical stakeholder rather than a CI-integrated scan.

## Install / Deploy

```bash
pip install scoutsuite
scout aws   # requires AWS credentials configured
```

## Common Commands

```bash
scout aws --report-dir ./report
scout azure --report-dir ./report
```

## Lab Exercise

Run ScoutSuite against the same lab cloud account used for [Prowler](prowler.md), and compare the two tools' reports for the same findings — useful for understanding when each format (CLI/compliance-mapped vs. browsable HTML) fits better.

## Related Tools

- [Prowler](prowler.md) — comparable multi-cloud alternative
