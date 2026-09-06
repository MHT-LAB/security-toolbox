# Secure & Harden

Auditing and locking down configurations before someone else finds the gap.

## 🏆 Top 15 (most widely used)

- **[Lynis](https://github.com/CISOfy/lynis)** — security auditing tool for Linux/Unix systems.
  *Use it:* run `lynis audit system` on every server image before it goes into production, and again on a recurring cron so drift gets caught, not just the initial build.
- **[OpenSCAP](https://github.com/OpenSCAP/openscap)** — compliance and vulnerability scanning against SCAP benchmarks.
- **[CIS Benchmarks / CIS-CAT Lite](https://www.cisecurity.org/cis-benchmarks)** — free, vendor-neutral hardening baselines; CIS-CAT Lite is free but not open-source.
- **[Trivy](https://github.com/aquasecurity/trivy)** — vulnerability and misconfiguration scanner for containers, IaC, and filesystems.
- **[OPNsense](https://github.com/opnsense/core)** — free, open-source firewall/router platform (pfSense's actively-forked sibling).
- **[Greenbone Community Edition (OpenVAS)](https://github.com/greenbone/openvas-scanner)** — free vulnerability scanning engine.
- **[DevSec Hardening Framework (Ansible)](https://github.com/dev-sec/ansible-collection-hardening)** — Ansible playbooks that codify OS/SSH/nginx hardening baselines.
- **[Chef InSpec](https://github.com/inspec/inspec)** — compliance-as-code framework for auditing infrastructure state.
- **[Checkov](https://github.com/bridgecrewio/checkov)** — static analysis for Terraform/CloudFormation/Kubernetes misconfigurations.
- **[kube-bench](https://github.com/aquasecurity/kube-bench)** — checks Kubernetes clusters against CIS Kubernetes Benchmark.
- **[kube-hunter](https://github.com/aquasecurity/kube-hunter)** — hunts for security weaknesses in Kubernetes clusters.
- **[Falco](https://github.com/falcosecurity/falco)** — runtime security/anomaly detection for containers and Kubernetes.
- **[ClamAV](https://github.com/Cisco-Talos/clamav)** — open-source antivirus/malware-scanning engine.
- **[Vuls](https://github.com/future-architect/vuls)** — agentless vulnerability scanner for Linux/FreeBSD.
- **[Semgrep](https://github.com/semgrep/semgrep)** — static analysis (SAST) for finding security bugs in source code before it ships.

## More tools worth knowing

- **[Docker Bench for Security](https://github.com/docker/docker-bench-security)** — checks Docker hosts/containers against CIS Docker Benchmark.
- **[Prowler](https://github.com/prowler-cloud/prowler)** — AWS/Azure/GCP security best-practices and compliance auditing.
- **[ScoutSuite](https://github.com/nccgroup/ScoutSuite)** — multi-cloud security-posture auditing tool.
- **[Grype](https://github.com/anchore/grype)** — vulnerability scanner for container images and filesystems.
- **[Syft](https://github.com/anchore/syft)** — generates SBOMs (software bill of materials) from images/filesystems.
- **[Bandit](https://github.com/PyCQA/bandit)** — SAST tool specifically for Python code.
- **[Gitleaks](https://github.com/gitleaks/gitleaks)** — scans git repos/history for hardcoded secrets before they leak.
- **[TruffleHog](https://github.com/trufflesecurity/trufflehog)** — deep secret-scanning across repos and live credentials verification.
- **[AIDE](https://github.com/aide/aide)** — file and directory integrity checker.
- **[rkhunter](https://github.com/Rootkit-Hunter/rkhunter)** — rootkit, backdoor, and local exploit scanner for *nix hosts.
- **[Firejail](https://github.com/netblue30/firejail)** — SUID sandbox that restricts what a Linux application can touch.

*General infrastructure guidance:* bake Lynis/OpenSCAP/CIS-CAT into the golden-image pipeline (run at build time, not just after deployment), gate CI on Checkov/Semgrep/Gitleaks so misconfigurations and secrets never reach `main`, and treat Falco/kube-bench as continuous runtime checks rather than one-time audits.
