# Secure & Harden

Auditing and locking down configurations before someone else finds the gap.

Every tool below has its own page under [`tools/`](tools/) with Overview, Install/Deploy, Common Commands, a concrete Lab Exercise, and Related Tools — not just a link out.

## 🏆 Top 15 (most widely used)

| Tool | What it does |
|---|---|
| [Lynis](tools/lynis.md) | Security auditing tool for Linux/Unix systems. |
| [OpenSCAP](tools/openscap.md) | Compliance and vulnerability scanning against SCAP benchmarks. |
| [CIS Benchmarks / CIS-CAT Lite](tools/cis-benchmarks.md) | Free, vendor-neutral hardening baselines. |
| [Trivy](tools/trivy.md) | Vulnerability and misconfiguration scanner for containers/IaC. |
| [OPNsense](tools/opnsense.md) | Free, open-source firewall/router platform. |
| [Greenbone Community Edition (OpenVAS)](tools/greenbone-openvas.md) | Free vulnerability scanning engine. |
| [DevSec Hardening Framework (Ansible)](tools/devsec-hardening.md) | Ansible playbooks codifying OS/SSH/nginx hardening. |
| [Chef InSpec](tools/chef-inspec.md) | Compliance-as-code framework for auditing infrastructure state. |
| [Checkov](tools/checkov.md) | Static analysis for Terraform/CloudFormation/Kubernetes. |
| [kube-bench](tools/kube-bench.md) | Checks Kubernetes clusters against CIS Kubernetes Benchmark. |
| [kube-hunter](tools/kube-hunter.md) | Hunts for security weaknesses in Kubernetes clusters. |
| [Falco](tools/falco.md) | Runtime security/anomaly detection for containers and Kubernetes. |
| [ClamAV](tools/clamav.md) | Open-source antivirus/malware-scanning engine. |
| [Vuls](tools/vuls.md) | Agentless vulnerability scanner for Linux/FreeBSD. |
| [Semgrep](tools/semgrep.md) | Static analysis (SAST) for finding security bugs in source code. |

## More tools worth knowing

| Tool | What it does |
|---|---|
| [Docker Bench for Security](tools/docker-bench.md) | Checks Docker hosts/containers against CIS Docker Benchmark. |
| [Prowler](tools/prowler.md) | AWS/Azure/GCP security best-practices and compliance auditing. |
| [ScoutSuite](tools/scoutsuite.md) | Multi-cloud security-posture auditing tool. |
| [Grype](tools/grype.md) | Vulnerability scanner for container images and filesystems. |
| [Syft](tools/syft.md) | Generates SBOMs from images/filesystems. |
| [Bandit](tools/bandit.md) | SAST tool specifically for Python code. |
| [Gitleaks](tools/gitleaks.md) | Scans git repos/history for hardcoded secrets. |
| [TruffleHog](tools/trufflehog.md) | Deep secret-scanning with live-credential verification. |
| [AIDE](tools/aide.md) | File and directory integrity checker. |
| [rkhunter](tools/rkhunter.md) | Rootkit, backdoor, and local exploit scanner. |
| [Firejail](tools/firejail.md) | SUID sandbox that restricts what an application can touch. |

*General infrastructure guidance:* bake [Lynis](tools/lynis.md)/[OpenSCAP](tools/openscap.md)/[CIS-CAT](tools/cis-benchmarks.md) into the golden-image pipeline (run at build time, not just after deployment), gate CI on [Checkov](tools/checkov.md)/[Semgrep](tools/semgrep.md)/[Gitleaks](tools/gitleaks.md) so misconfigurations and secrets never reach `main`, and treat [Falco](tools/falco.md)/[kube-bench](tools/kube-bench.md) as continuous runtime checks rather than one-time audits.
