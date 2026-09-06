# kube-hunter

Hunts for security weaknesses in Kubernetes clusters — takes an attacker's perspective rather than kube-bench's compliance-checklist approach.

**Links:** [GitHub](https://github.com/aquasecurity/kube-hunter) · [Docs](https://aquasecurity.github.io/kube-hunter/)

## Overview

Where kube-bench checks configuration against a standard, kube-hunter actively probes a cluster the way an attacker would — looking for exposed dashboards, insecure API server access, and known CVEs — from inside or outside the cluster network.

## Install / Deploy

```bash
docker run -it --rm aquasec/kube-hunter
# or: pip install kube-hunter
```

## Common Commands

```bash
kube-hunter --remote <cluster-ip>
kube-hunter --pod   # run from inside a pod for internal-perspective testing
```

## Lab Exercise

Run kube-hunter against a lab Kubernetes cluster from both outside (`--remote`) and inside (`--pod`) perspectives, and compare what's discoverable from each vantage point.

## Related Tools

- [kube-bench](kube-bench.md) — complementary compliance-checklist scan
