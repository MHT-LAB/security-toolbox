# JoeSandbox

Commercial automated malware sandbox with a free/community submission tier — detailed behavioral analysis reports beyond what a signature-based AV check gives you.

**Links:** [Official site](https://www.joesandbox.com) — SaaS, no public repo.

## Overview

JoeSandbox detonates a submitted sample and produces a detailed behavioral report — API calls, network indicators, and a threat score — with a free community tier that's rate-limited compared to the commercial product.

## Install / Deploy

```text
Free account registration at joesandbox.com's community edition for limited submissions.
```

## Common Commands

Primarily web-UI driven; a REST API is available for paid tiers.

## Lab Exercise

Submit a sample you've already run through [VirusTotal](virustotal.md) to JoeSandbox's community tier and compare the depth of behavioral detail against VT's own sandbox summary.

## Related Tools

- [VirusTotal](virustotal.md) · [Hybrid Analysis](hybrid-analysis.md) — comparable free-tier sandboxes
- [CAPEv2](capev2.md) — self-hosted alternative with no submission limits
