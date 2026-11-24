# 🦉 OK8sRbac

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OScan-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-orange?style=flat-square"/>
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

This tool is part of the **OwlSec** suite — a collection of 275+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

Proprietary — © 2026 Owlsec LLC. All rights reserved.

*Tools are distributed as pre-built executables. Source code is proprietary.*

---

## 🔍 Verification & Transparency

This tool is closed-source. These files let you see exactly what is inside it,
without the source:

- [`SBOM.cdx.json`](SBOM.cdx.json) — CycloneDX inventory: SHA-256 of this
  binary, bundled CPython version, and every bundled library with its exact
  version and license. Feed it to Grype, Trivy or Dependency-Track to audit
  our dependencies for CVEs yourself.
- [`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md) — the full license text
  of every third-party component, extracted from this binary.

**No telemetry, no analytics, no licence check-in.** This tool does not phone
home. Verify that claim yourself:

```bash
sudo strace -f -e trace=network ./OK8sRbac --help   # watch every network call
firejail --net=none ./OK8sRbac --help               # deny the network entirely
```

Release signing, GPL compliance and vulnerability reporting:
[**TRUST.md**](https://github.com/owlsecx/owl-os/blob/main/TRUST.md)
