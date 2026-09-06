# Checkov

Static analysis for Terraform/CloudFormation/Kubernetes misconfigurations — catches insecure infrastructure-as-code before it's ever deployed.

**Links:** [GitHub](https://github.com/bridgecrewio/checkov) · [Docs](https://www.checkov.io)

## Overview

Checkov scans IaC files (Terraform, CloudFormation, Kubernetes YAML, Dockerfiles) against hundreds of built-in policies — a publicly-readable S3 bucket or an open security group gets flagged before `terraform apply` ever runs, not after.

## Install / Deploy

```bash
pip install checkov
```

## Common Commands

```bash
checkov -d ./terraform/
checkov -f docker-compose.yml
checkov --framework kubernetes -d ./k8s-manifests/
```

## Lab Exercise

Run Checkov against a Terraform config for your homelab's cloud resources (if any) or a sample public IaC repo, fix the highest-severity finding, and re-run to confirm it's resolved — then wire it into a CI pipeline as a gate.

## Related Tools

- [Trivy](trivy.md) — overlapping IaC/config scanning capability
- [tfsec](https://github.com/aquasecurity/tfsec) — Terraform-specific scanner, now folded into Trivy
