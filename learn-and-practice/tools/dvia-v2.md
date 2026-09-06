# DVIA-v2

Damn Vulnerable iOS App — for mobile security practice, covering common iOS-specific vulnerability classes (insecure storage, jailbreak detection bypass, weak crypto).

**Links:** [GitHub](https://github.com/prateek147/DVIA-v2)

## Overview

DVIA-v2 is a deliberately vulnerable iOS app for practicing mobile-specific security testing — insecure local data storage, broken cryptography, and runtime manipulation, distinct from the web-focused vulnerabilities elsewhere in this repo.

## Install / Deploy

```text
Requires a Mac with Xcode; clone the repo, open the project, and build/run
on a jailbroken device or the iOS Simulator (some checks require a jailbroken device).
```

## Common Commands

Mobile-specific tooling (not otherwise covered in this repo) such as Frida/Objection for runtime instrumentation.

## Lab Exercise

Build and run DVIA-v2, and work through its insecure-data-storage challenge by examining the app's local storage directly on a jailbroken device or simulator.

## Related Tools

- [OVAA](ovaa.md) — Android equivalent
