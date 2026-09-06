# CIS Benchmarks / CIS-CAT Lite

Free, vendor-neutral hardening baselines — the reference standard most compliance frameworks and auditors already assume. CIS-CAT Lite is free to use but not open-source.

**Links:** [Official site](https://www.cisecurity.org/cis-benchmarks) — CIS-CAT Lite download requires free registration.

## Overview

CIS publishes detailed, versioned hardening benchmarks for dozens of OSes, applications, and cloud platforms. CIS-CAT Lite is CIS's own free assessment tool that scores a system against a chosen benchmark (the Pro version covers more benchmarks and adds remediation content).

## Install / Deploy

```text
Register for a free CIS SecureSuite membership at cisecurity.org to download CIS-CAT Lite,
then run the provided assessor-cli script against your target benchmark.
```

## Common Commands

```bash
./Assessor-CLI.sh -a -b benchmark.xml -r results/
```

## Lab Exercise

Download the CIS Benchmark PDF for your lab's OS, pick five controls, manually verify (or fix) them on a lab VM, then run CIS-CAT Lite to confirm your manual work matches the automated assessment.

## Related Tools

- [OpenSCAP](openscap.md) — can evaluate against CIS-derived SCAP content directly
- [kube-bench](kube-bench.md) — CIS Benchmark evaluation specifically for Kubernetes
