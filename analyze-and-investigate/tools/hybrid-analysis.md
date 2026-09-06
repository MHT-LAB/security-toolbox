# Hybrid Analysis

Free, CrowdStrike-run automated malware sandbox (Falcon Sandbox) — solid free-tier alternative to VirusTotal/JoeSandbox for behavioral detonation reports.

**Links:** [Official site](https://www.hybrid-analysis.com) — SaaS, no public repo.

## Overview

Hybrid Analysis runs CrowdStrike's Falcon Sandbox engine with a genuinely useful free tier, producing detailed behavioral reports (network, registry, dropped files) plus a threat score — a good complementary check alongside VirusTotal.

## Install / Deploy

```text
Free account registration at hybrid-analysis.com; API key available for the free tier.
```

## Common Commands

```bash
curl -H "api-key: $HA_API_KEY" -F "file=@sample.exe" -F "environment_id=120" \
  https://www.hybrid-analysis.com/api/v2/submit/file
```

## Lab Exercise

Submit the same sample used in the [JoeSandbox](joesandbox.md) exercise here as well, and compare all three free sandbox reports (VirusTotal, JoeSandbox, Hybrid Analysis) side by side to see how much they agree.

## Related Tools

- [VirusTotal](virustotal.md) · [JoeSandbox](joesandbox.md) — comparable free-tier sandboxes
