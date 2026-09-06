# Trivy

Vulnerability and misconfiguration scanner for containers, IaC, and filesystems — one binary covers container images, Terraform/CloudFormation, Kubernetes manifests, and SBOMs.

**Links:** [GitHub](https://github.com/aquasecurity/trivy) · [Docs](https://aquasecurity.github.io/trivy/)

## Overview

Trivy scans a huge range of targets — container images, git repos, filesystems, Kubernetes clusters, and IaC templates — for known CVEs and misconfigurations, making it a good default first scanner to add to any CI pipeline.

## Install / Deploy

```bash
sudo apt install trivy
# or: brew install trivy
```

## Common Commands

```bash
trivy image nginx:latest
trivy fs --security-checks vuln,config .
trivy config ./terraform/
```

## Lab Exercise

Run `trivy image` against a container image you've built for your homelab (e.g. a service from [network-and-homelab](../../network-and-homelab/README.md)), and fix the highest-severity CVE it finds by bumping the base image version.

## Related Tools

- [Grype](grype.md) · [Syft](syft.md) — complementary scanning/SBOM tools
- [Checkov](checkov.md) — deeper IaC-specific alternative
