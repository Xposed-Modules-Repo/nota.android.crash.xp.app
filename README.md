# CrashCenter / 崩溃中心

Xposed module that intercepts **uncaught Java exceptions** in hooked apps so the process does not exit.

**This module swallows crashes — it does not fix bugs.** Unexpected behavior may occur. Use only on apps you understand; avoid system apps unless necessary.

## Requirements

- Android 8.0+ (API 26+)
- LSPosed or compatible Xposed framework
- Enable this module in the manager and **reboot**
- Set **scope** to target apps in LSPosed; configure observe / intercept per app inside CrashCenter

## Features

- **Intercept** — replace uncaught exception handler in scoped apps (app keeps running)
- **Observe** — record crash events without swallowing exceptions
- Per-app managed list, scope mode, crash notification and detail view
- Crash history, statistics, rule-based stack analysis
- Logcat import (root multi-buffer or SAF file), export crash records as zip
- CodeEditor-based stack trace viewer

## Source & support

- Source: https://github.com/TIIEHenry/CrashCenter
- Issues: https://github.com/TIIEHenry/CrashCenter/issues
- User guide: https://github.com/TIIEHenry/CrashCenter/blob/main/docs/guides/usage.md
