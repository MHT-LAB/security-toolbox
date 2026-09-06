# OpenSCAP

Compliance and vulnerability scanning against SCAP benchmarks — automated, standards-based auditing (NIST, DISA STIG, CIS) rather than Lynis's more general checks.

**Links:** [GitHub](https://github.com/OpenSCAP/openscap) · [Docs](https://www.open-scap.org/getting-started/)

## Overview

OpenSCAP evaluates a system against formal SCAP-format profiles (e.g. a DISA STIG or CIS benchmark), producing a pass/fail report per control — the tool of choice when you need to demonstrate compliance against a named standard rather than general hardening.

## Install / Deploy

```bash
sudo apt install openscap-scanner scap-security-guide
```

## Common Commands

```bash
oscap xccdf eval --profile cis --results results.xml \
  /usr/share/xml/scap/ssg/content/ssg-ubuntu2204-xccdf.xml
oscap xccdf generate report results.xml > report.html
```

## Lab Exercise

Run an OpenSCAP CIS-profile evaluation against a lab VM, review the HTML report for failed controls, remediate the top few manually, and re-scan to confirm the pass rate improves.

## Related Tools

- [Lynis](lynis.md) — lighter, non-standards-bound alternative
- [CIS Benchmarks](cis-benchmarks.md) — the actual standard OpenSCAP can evaluate against
