# 🦉 OSeLinux

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OScan-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OSeLinux** — Offline SELinux Configuration & Policy

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

Offline SELinux configuration & policy posture auditor

---

## ✨ Features

- /etc/selinux/config parser — SELINUX=, SELINUXTYPE=, SETLOCALDEFS, REQUIRESEUSERS, duplicate / typo keys
- Runtime snapshot reader — /sys/fs/selinux/enforce, policyvers, deny_unknown, checkreqprot, mls, sestatus
- Boolean dump parser — getsebool -a, semanage boolean -l, setsebool -P scripts, booleans(.local), CIL
- Curated high-risk boolean catalogue (~45 booleans) + "expected-on" hardening booleans (secure_mode_*)
- fcontext parser — semanage fcontext -l, file_contexts (+ .local / .homedirs); coverage of critical paths
- Module inventory — semodule -l / --list-modules=full, store directory walk, custom .te / .cil source review (dontaudit removal, permissive, allow unconfined)
- Permissive domain list (semanage permissive -l)
- SELinux user / login mapping review (unconfined_u)
- Process label hints from ps -eZ dumps (unconfined_t)
- Kernel cmdline / GRUB review (selinux=0, enforcing=0)
- CIS / DISA STIG / CWE / MITRE ATT&CK mapping
- Score + A+…F grade, severity filter, --fail-on gate
- Export TXT / Markdown / JSON / CSV / SARIF 2.1.0
- Built-in self-test (--demo) on a synthetic tree

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OSeLinux
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
