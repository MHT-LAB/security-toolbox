# Docker Bench for Security

Checks Docker hosts/containers against CIS Docker Benchmark — a lightweight script version of the compliance-check pattern kube-bench applies to Kubernetes.

**Links:** [GitHub](https://github.com/docker/docker-bench-security)

## Overview

Docker Bench runs a series of automated checks against a Docker host's configuration (daemon settings, container runtime options, image/file permissions) and reports pass/warn/info per CIS Docker Benchmark control.

## Install / Deploy

```bash
git clone https://github.com/docker/docker-bench-security.git
cd docker-bench-security
sudo sh docker-bench-security.sh
```

## Common Commands

```bash
sudo sh docker-bench-security.sh -c container_images,container_runtime
```

## Lab Exercise

Run Docker Bench against your homelab's Docker host, fix a flagged warning (e.g. a container running as root unnecessarily), and re-run to confirm the check now passes.

## Related Tools

- [kube-bench](kube-bench.md) — same concept for Kubernetes instead of standalone Docker
- [Trivy](trivy.md) — complementary image vulnerability scanning
