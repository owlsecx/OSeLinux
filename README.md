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

OSeLinux is an offline, read-only auditor for SELinux configuration and policy posture. It parses /etc/selinux/config, runtime snapshots, boolean dumps, fcontext listings and module inventories to assess enforcement mode, risky booleans and permissive domains. Findings are scored and mapped to CIS, STIG, CWE and MITRE ATT&CK.

---

## ✨ Features

- /etc/selinux/config parser and runtime snapshot reader (enforce, policyvers, sestatus)
- Boolean dump parsing with a curated high-risk boolean catalogue
- fcontext and file-context coverage analysis for critical paths
- Module inventory review with custom .te/.cil source checks and permissive-domain listing
- SELinux user/login mapping, process-label hints and kernel cmdline/GRUB review
- CIS/STIG/CWE/MITRE mapping with scoring, A+ to F grade and a CI fail-on gate

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OSeLinux --scan
./OSeLinux --config /etc/selinux/config --booleans booleans.txt
./OSeLinux --root /mnt/collected --fail-on high
./OSeLinux --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
