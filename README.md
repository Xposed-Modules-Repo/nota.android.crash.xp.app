# CrashCenter / 稳定性中心

[English](#english) · [中文](#中文)

---

## English

Xposed module that **intercepts uncaught Java exceptions** in hooked apps so the process does not exit.

> **Warning:** This module **swallows crashes — it does not fix bugs.** Unexpected behavior may occur. Use only on apps you understand; avoid system apps unless necessary.

### Requirements

- Android 8.0+ (API 26+)
- [LSPosed](https://github.com/LSPosed/LSPosed) or compatible Xposed framework
- Enable this module in the manager and **reboot**
- Set **scope** to target apps in LSPosed; configure observe / intercept inside CrashCenter

### Features

| Area | Description |
|------|-------------|
| **Intercept** | Replace uncaught exception handler — app keeps running after a crash |
| **Observe** | Record crash events **without** swallowing exceptions |
| **Config** | Per-app managed list, scope mode, package visibility |
| **History** | Paged crash list, statistics, per-app drill-down |
| **Analysis** | Rule engine + built-in signature library on stack traces |
| **Logcat** | Root multi-buffer or SAF file import; crash / ANR hints |
| **Export** | Export crash records as zip (SAF) |
| **Detail UI** | CodeEditor-based stack trace viewer |

### Scope vs in-app toggles

Both must be configured:

1. **LSPosed scope** — whether the module is injected into the target app process
2. **CrashCenter switches** — whether to **intercept** (keep alive) or **observe only** (log and allow exit)

### Links

- Source: https://github.com/TIIEHenry/CrashCenter
- Issues: https://github.com/TIIEHenry/CrashCenter/issues
- User guide: https://github.com/TIIEHenry/CrashCenter/blob/main/docs/guides/usage.md

---

## 中文

基于 Xposed 的模块，在已 hook 的应用中**拦截 Java 层未捕获异常**，避免进程因崩溃而退出。

> **注意：** 本模块**吞掉异常，不修复错误**。可能导致不可预期行为。建议仅对熟悉的应用使用；非必要请勿作用于系统应用。

### 环境要求

- Android 8.0+（API 26+）
- [LSPosed](https://github.com/LSPosed/LSPosed) 或兼容的 Xposed 框架
- 在管理器中启用本模块并**重启**
- 在 LSPosed 中勾选目标应用作用域；在稳定性中心内配置**观测 / 拦截**

### 功能概览

| 能力 | 说明 |
|------|------|
| **拦截** | 替换未捕获异常处理器，崩溃后进程继续运行 |
| **观测** | 记录崩溃事件，**不**阻止进程退出 |
| **配置** | 受管应用列表、作用域模式、包可见性 |
| **历史** | 崩溃列表分页、统计、按应用下钻 |
| **分析** | 规则引擎 + 内置签名库，辅助读堆栈 |
| **Logcat** | Root 多 buffer 或 SAF 导入；崩溃 / ANR 提示 |
| **导出** | SAF 导出崩溃记录 zip |
| **详情** | CodeEditor 堆栈浏览 |

### 作用域与应用内开关

两套配置**都要**理解：

1. **LSPosed 作用域** — 模块是否注入目标应用进程（外层门控）
2. **稳定性中心开关** — **拦截**（续命）或**仅观测**（记录后允许退出）

### 链接

- 源码：https://github.com/TIIEHenry/CrashCenter
- 反馈：https://github.com/TIIEHenry/CrashCenter/issues
- 使用指南：https://github.com/TIIEHenry/CrashCenter/blob/main/docs/guides/usage.md
