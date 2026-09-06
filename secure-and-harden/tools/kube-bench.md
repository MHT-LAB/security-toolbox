# kube-bench

Checks Kubernetes clusters against CIS Kubernetes Benchmark — an automated, cluster-aware evaluation instead of manually reading the benchmark PDF.

**Links:** [GitHub](https://github.com/aquasecurity/kube-bench) · [Docs](https://aquasecurity.github.io/kube-bench/)

## Overview

kube-bench runs directly against a live cluster's control-plane and node configuration, checking each item from the CIS Kubernetes Benchmark and reporting pass/fail/warn per control — usually the first tool run against any new cluster.

## Install / Deploy

```bash
docker run --pid=host -v /etc:/etc:ro -v /var:/var:ro \
  --rm aquasec/kube-bench:latest
# or as a Kubernetes Job — see repo's job-*.yaml manifests
```

## Common Commands

```bash
kube-bench run --targets master,node
kube-bench run --benchmark cis-1.24
```

## Lab Exercise

Run kube-bench against a lab Kubernetes cluster (k3s/kind/minikube all work), fix a failed control (e.g. an insecure kubelet flag), and re-run to confirm it now passes.

## Related Tools

- [kube-hunter](kube-hunter.md) — complementary offensive-style cluster scan
- [Falco](falco.md) — runtime detection layer once the cluster is hardened
