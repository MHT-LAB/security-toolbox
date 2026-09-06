# Bandit

SAST tool specifically for Python code — catches common Python security anti-patterns (hardcoded passwords, `eval()` usage, weak crypto, shell injection via `subprocess`).

**Links:** [GitHub](https://github.com/PyCQA/bandit) · [Docs](https://bandit.readthedocs.io)

## Overview

Bandit is narrower than Semgrep (Python-only) but fast and easy to add directly to a Python project's CI — a good first SAST tool for any Python codebase before reaching for something broader.

## Install / Deploy

```bash
pip install bandit
```

## Common Commands

```bash
bandit -r ./my_project/
bandit -r . -f json -o results.json
```

## Lab Exercise

Run Bandit against any Python project you maintain (or a deliberately vulnerable sample repo), fix the highest-severity finding, and add Bandit as a pre-commit hook so future commits are checked automatically.

## Related Tools

- [Semgrep](semgrep.md) — broader, multi-language alternative
