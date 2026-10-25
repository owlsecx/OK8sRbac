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

OK8sRbac is an offline Kubernetes RBAC and privilege-path analyzer. It inventories Roles, ClusterRoles, bindings, and ServiceAccounts from YAML, runs detection rules, and traces escalation chains with who-can / what-can queries. Results map to MITRE ATT&CK and CIS 5.1.x and export to TXT, Markdown, JSON, CSV, SARIF, or DOT.

---

## ✨ Features

- Stdlib YAML parser with RBAC inventory (Roles, Bindings, SAs, aggregationRule, workload→SA mapping)
- Detection rule set covering privilege escalation with BFS path analysis
- `--who-can` / subject queries with optional namespace filter
- Escalation path listing and optional DOT graph export
- MITRE ATT&CK and CIS 5.1.x mapping; min-severity and fail-on CI gates
- Exports TXT / MD / JSON / CSV / SARIF / DOT; `--demo` self-test and rule catalogue

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OK8sRbac --path ./manifests --scan
./OK8sRbac -p rbac.yaml --who-can get secrets --namespace prod
./OK8sRbac --paths --format sarif -o rbac.sarif --fail-on high
./OK8sRbac --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
