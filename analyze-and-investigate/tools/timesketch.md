# Timesketch

Collaborative timeline analysis, pairs with Plaso output — a web UI for multiple analysts to review, annotate, and filter a shared timeline.

**Links:** [GitHub](https://github.com/google/timesketch) · [Docs](https://timesketch.org)

## Overview

Once [Plaso](plaso.md) builds a raw timeline, Timesketch gives a team a shared, searchable, annotatable view of it — tag events, add comments, and filter by time range collaboratively instead of everyone working from their own CSV export.

## Install / Deploy

```bash
git clone https://github.com/google/timesketch.git
cd timesketch/docker && docker-compose up -d
```

## Common Commands

```bash
tsctl import-timeline --file timeline.plaso --index name
```

## Lab Exercise

Import a Plaso timeline from your [Plaso](plaso.md) lab exercise into Timesketch, then practice filtering and tagging events around your investigation's key moment — this is the workflow real DFIR teams use to hand off findings between analysts.

## Related Tools

- [Plaso / log2timeline](plaso.md) — the upstream timeline generator
