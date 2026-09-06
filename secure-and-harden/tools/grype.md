# Grype

Vulnerability scanner for container images and filesystems — from the same team as Syft, focused specifically on fast, accurate CVE matching.

**Links:** [GitHub](https://github.com/anchore/grype) · [Docs](https://github.com/anchore/grype#grype)

## Overview

Grype scans a container image or directory and reports known vulnerabilities in installed packages — often paired with [Syft](syft.md) (Grype can scan a Syft-generated SBOM directly instead of re-scanning the image).

## Install / Deploy

```bash
curl -sSfL https://raw.githubusercontent.com/anchore/grype/main/install.sh | sh -s -- -b /usr/local/bin
```

## Common Commands

```bash
grype nginx:latest
grype sbom:./sbom.json     # scan a Syft-generated SBOM
grype dir:./my-project
```

## Lab Exercise

Generate an SBOM for a homelab container image with [Syft](syft.md), then scan that SBOM with Grype instead of re-scanning the image directly — this SBOM-first pattern is faster for repeated scans of the same image.

## Related Tools

- [Syft](syft.md) — generates the SBOM Grype can consume
- [Trivy](trivy.md) — overlapping all-in-one alternative
