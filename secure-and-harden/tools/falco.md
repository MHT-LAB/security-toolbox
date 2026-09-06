# Falco

Runtime security/anomaly detection for containers and Kubernetes — watches system calls in real time and alerts on suspicious behavior inside a running container.

**Links:** [GitHub](https://github.com/falcosecurity/falco) · [Docs](https://falco.org/docs/)

## Overview

Falco is the runtime counterpart to kube-bench/kube-hunter's point-in-time checks — it watches live syscall activity and alerts when a container does something a rule flags as suspicious (a shell spawned inside a container that shouldn't have one, an unexpected outbound connection, a write to a sensitive path).

## Install / Deploy

```bash
# Kubernetes (Helm):
helm repo add falcosecurity https://falcosecurity.github.io/charts
helm install falco falcosecurity/falco --namespace falco --create-namespace
```

## Common Commands

```bash
falco -r /etc/falco/falco_rules.yaml
kubectl logs -n falco -l app.kubernetes.io/name=falco
```

## Lab Exercise

Deploy Falco on a lab Kubernetes cluster, exec into a running pod to spawn a shell (`kubectl exec -it <pod> -- /bin/sh`), and confirm Falco's default rules flag the unexpected shell activity.

## Related Tools

- [kube-bench](kube-bench.md) · [kube-hunter](kube-hunter.md) — point-in-time complements to Falco's runtime watch
