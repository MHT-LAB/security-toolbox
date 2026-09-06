# Hayabusa

Fast Windows event log timeline/detection tool, Sigma-compatible — Rust-based, built for speed against very large log sets.

**Links:** [GitHub](https://github.com/Yamato-Security/hayabusa) · [Docs](https://github.com/Yamato-Security/hayabusa/wiki)

## Overview

Similar goal to Chainsaw (Sigma rules against EVTX), Hayabusa emphasizes speed and produces a timeline-style output with severity scoring, making it convenient for quickly triaging which events across a large log set deserve attention first.

## Install / Deploy

```text
Download the release binary from the GitHub releases page.
```

## Common Commands

```bash
./hayabusa csv-timeline -d evtx_folder/ -o results.csv
./hayabusa -h   # list all subcommands
```

## Lab Exercise

Run Hayabusa against the same EVTX export used in the [Chainsaw](chainsaw.md) exercise, sort the resulting CSV by severity, and compare which tool surfaced the relevant finding higher/faster.

## Related Tools

- [Chainsaw](chainsaw.md) — closest direct alternative
