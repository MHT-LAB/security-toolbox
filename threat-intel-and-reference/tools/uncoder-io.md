# Uncoder IO (SOC Prime)

Free browser-based converter between Sigma, Roota, and native SIEM/EDR query languages — write a detection once, translate it without installing anything.

**Links:** [Official site](https://uncoder.io)

## Overview

Uncoder IO does in the browser what `sigma-cli` does locally — paste a Sigma rule, pick a target platform (Splunk, Elastic, Microsoft Sentinel, and more), and get back a converted query, with no local Sigma toolchain setup required.

## Install / Deploy

```text
No installation — browse to uncoder.io and paste a rule directly.
```

## Common Commands

Not applicable — paste-and-convert web tool.

## Lab Exercise

Take a [Sigma](../../detect-and-respond/tools/sigma.md) rule from the SigmaHQ repo, convert it via Uncoder IO to your SIEM's query language, and compare the output against what `sigma-cli` produces locally for the same rule.

## Related Tools

- [Sigma](../../detect-and-respond/tools/sigma.md) — the rule format this converts
