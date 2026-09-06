# Syft

Generates SBOMs (software bills of materials) from images/filesystems — inventories every package and library in a container image or directory.

**Links:** [GitHub](https://github.com/anchore/syft) · [Docs](https://github.com/anchore/syft#syft)

## Overview

Syft catalogs exactly what's inside a container image or filesystem — package names, versions, and licenses — in standard SBOM formats (SPDX, CycloneDX). SBOMs are increasingly a compliance requirement, and pairing Syft's output with [Grype](grype.md) gives fast repeat vulnerability scanning without re-analyzing the image each time.

## Install / Deploy

```bash
curl -sSfL https://raw.githubusercontent.com/anchore/syft/main/install.sh | sh -s -- -b /usr/local/bin
```

## Common Commands

```bash
syft nginx:latest
syft nginx:latest -o spdx-json > sbom.json
syft dir:./my-project
```

## Lab Exercise

Generate an SBOM for a homelab-built container image, review what packages it lists that you didn't expect to be there, and feed the SBOM into [Grype](grype.md) for vulnerability scanning.

## Related Tools

- [Grype](grype.md) — vulnerability scanning against the SBOM this produces
