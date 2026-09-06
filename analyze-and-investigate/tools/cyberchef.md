# CyberChef

GCHQ's "cyber Swiss Army knife" for decoding/transforming data, runs entirely in-browser — chain operations (Base64, XOR, hex, regex, and hundreds more) into a reusable "recipe."

**Links:** [GitHub](https://github.com/gchq/CyberChef) · [Hosted version](https://gchq.github.io/CyberChef/)

## Overview

CyberChef lets you drag-and-drop a chain of data transformations — decode Base64, then XOR with a key, then extract strings — without writing a script for a one-off task. Recipes are shareable/saveable, making it useful for documenting exactly how you decoded something for a report.

## Install / Deploy

```text
Use the hosted version at gchq.github.io/CyberChef, or download the
self-contained HTML file from the GitHub releases page to run fully offline.
```

## Common Commands

CyberChef is drag-and-drop; build a "recipe" by chaining operations from the left panel (e.g. From Base64 → XOR → Extract Strings).

## Lab Exercise

Take an obfuscated PowerShell command (e.g. `-EncodedCommand` output, a common technique after [PowerSploit](../../test-and-exploit/tools/powersploit.md)/Empire usage) and build a CyberChef recipe to decode it back to readable script.

## Related Tools

- [FLOSS](floss.md) — complementary string-extraction tool for compiled binaries
