# OVAA

Oversecured Vulnerable Android App — for mobile security practice, the Android counterpart to DVIA-v2's iOS focus.

**Links:** [GitHub](https://github.com/oversecured/ovaa)

## Overview

OVAA is a deliberately vulnerable Android app covering common Android-specific issues (insecure IPC, exported components, insecure storage) — built by Oversecured specifically to demonstrate real-world Android vulnerability patterns.

## Install / Deploy

```bash
git clone https://github.com/oversecured/ovaa.git
# Build with Android Studio, install the APK on an emulator or test device
```

## Common Commands

Mobile-specific tooling such as `adb`, jadx (APK decompilation), or Frida for runtime analysis.

## Lab Exercise

Install OVAA on an Android emulator, use `adb` to inspect its exported components, and identify which ones are exploitable via a malicious companion app.

## Related Tools

- [DVIA-v2](dvia-v2.md) — iOS equivalent
