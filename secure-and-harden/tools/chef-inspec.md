# Chef InSpec

Compliance-as-code framework for auditing infrastructure state — write human-readable tests describing what "compliant" looks like, run them against real systems.

**Links:** [GitHub](https://github.com/inspec/inspec) · [Docs](https://docs.chef.io/inspec/)

## Overview

InSpec tests read almost like plain English ("describe sshd_config do its('PermitRootLogin') { should eq 'no' } end") and can run locally, over SSH, or against cloud APIs — a good fit for verifying that hardening (like the DevSec Ansible roles) actually took effect.

## Install / Deploy

```bash
curl https://omnitruck.chef.io/install.sh | sudo bash -s -- -P inspec
```

## Common Commands

```bash
inspec exec my_profile/ -t ssh://user@target
inspec exec https://github.com/dev-sec/linux-baseline
```

## Lab Exercise

Run the community `dev-sec/linux-baseline` InSpec profile against a lab VM you hardened with the [DevSec Ansible roles](devsec-hardening.md), and confirm it passes — then intentionally break one hardening setting and confirm InSpec catches the regression.

## Related Tools

- [DevSec Hardening Framework](devsec-hardening.md) — the hardening this verifies
- [OpenSCAP](openscap.md) — comparable compliance-verification alternative
