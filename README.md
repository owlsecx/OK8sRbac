# 🦉 OK8sRbac

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OScan-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OK8sRbac** — Offline Kubernetes RBAC & Privilege-Path Analyzer

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

Offline Kubernetes RBAC & privilege-path analyzer

---

## ✨ Features

- Stdlib YAML parser + RBAC inventory (Roles, Bindings, SAs, aggregationRule, workload→SA mapping)
- 34 detection rules, privilege-escalation BFS paths
- who-can / what-can queries, MITRE + CIS 5.1.x mapping
- Exports TXT/MD/JSON/CSV/SARIF + DOT graph; --demo ═══════════════════════════════════════════════════════════════ ANSI COLOUR SYSTEM ═══════════════════════════════════════════════════════════════

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OK8sRbac
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
