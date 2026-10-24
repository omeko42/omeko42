<div align="right">
  <b>🌐 Language / Bahasa:</b> &nbsp;
  <a href="https://github.com/omeko42/omeko42/blob/main/README.md"><b>🇬🇧 English (Default)</b></a> &nbsp;|&nbsp;
  <a href="https://github.com/omeko42/omeko42/blob/main/README.id.md">🇮🇩 Bahasa Indonesia</a>
</div>

# Eko Agung (`@omeko42`)
### Full-Stack Software Engineer & System Architect
*Founder of **CAS (Community Anggota Serse — 1,024+ Members)** & Lead Architect of **Big Data Binops (BDB)***

[![Flagship Platform](https://img.shields.io/badge/Flagship%20Platform-Big%20Data%20Binops%20(BDB)%20v2.5-1E40AF.svg?style=flat-square)](https://github.com/omeko42/big-data-binops)
[![Community](https://img.shields.io/badge/Community-CAS%20(1,024%2B%20Active%20Members)-25D366.svg?style=flat-square&logo=whatsapp&logoColor=white)](https://github.com/omeko42/big-data-binops)
[![Production Scale](https://img.shields.io/badge/Production%20DB-68.89M%2B%20Rows%20%7C%20171%20Tables-336791.svg?style=flat-square&logo=postgresql&logoColor=white)](https://github.com/omeko42/big-data-binops/blob/main/database/schema/DATABASE_INVENTORY.md)
[![Analytical Latency](https://img.shields.io/badge/Analytical%20Latency-%3C100ms%20(Snapshot%20Engine)-10B981.svg?style=flat-square)](https://github.com/omeko42/big-data-binops/blob/main/ARCHITECTURE.md)
[![Security](https://img.shields.io/badge/Security-FIDO2%20WebAuthn%20%2B%20TOTP%202FA-059669.svg?style=flat-square&logo=riotgames&logoColor=white)](https://github.com/omeko42/big-data-binops/blob/main/SECURITY.md)

---

## 👋 Executive Profile

I am an **Operational Data Analyst turned Full-Stack Software Engineer and System Architect**, specializing in high-scale operational data governance, distributed relational database engineering, and zero-trust enterprise web systems.

Starting my journey on the front lines of national operational data analysis at **Biro Pembinaan dan Operasional (Robinopsnal) Bareskrim Polri**, I experienced firsthand the complexity of reconciling multi-million-row law enforcement records across Indonesia. Rather than treating data discrepancies as purely administrative problems, I transitioned into full-stack systems engineering to solve them structurally:

1. **Founded CAS (*Community Anggota Serse*)**: Built an organic, bottom-up operational community uniting **1,024+ active criminal investigation personnel, operators, Kanit Reskrim Polsek, and Kaur Binops (KBO)** across Indonesia via tactical WhatsApp groups and the in-app **SHARESE** forum — creating a direct real-time feedback loop between field investigators and core engineering.
2. **Architected Big Data Binops (BDB)**: Designed and engineered a sovereign, enterprise-grade operational data platform from the ground up — consolidating multi-source law enforcement records, eliminating double data entry (*zero double-input*), and delivering sub-100ms national analytical dashboards across **Mabes Polri → 36 Polda → 508+ Polres → 4,900+ Polsek**.

---

## 🏛️ Flagship Engineering Portfolio: [Big Data Binops (BDB) — Powered by CAS (Community Anggota Serse)](https://github.com/omeko42/big-data-binops)

[**`omeko42/big-data-binops`**](https://github.com/omeko42/big-data-binops) is a production law enforcement data governance, 4-tier case lifecycle management, and document automation platform (**🇮🇩 [Baca Dokumentasi Bahasa Indonesia](https://github.com/omeko42/big-data-binops/blob/main/README.id.md)** | **🇬🇧 [Read English Documentation](https://github.com/omeko42/big-data-binops/blob/main/README.md)**).

### 📊 Production Scale at a Glance
| Domain | Verified Production Scale | Engineering Highlights |
| :--- | :--- | :--- |
| **Database Scale** | **~68.89 Million Active Rows** | **171 active PostgreSQL tables**, **433 indexes** (`B-Tree`, `GIN pg_trgm`), **7 PL/pgSQL functions**, **5 real-time triggers**, and **90 sequential migrations**. |
| **National Case Lifecycle** | **2.84+ Million Police Reports (LP)** | Automated ingestion from **DORS Stamaops Polri (Staf Utama Kapolri Bidang Operasi)** into immutable JSONB staging → normalized relational core across **14,217 Satker nodes**. |
| **Entity & Evidence Graph** | **11.16M+ Parties & 5.84M+ Evidence Items** | Cross-province NIK/NRP entity resolution, multi-Polda syndicate scoring, and dual-source national evidence tracking. |
| **Forensic Auditability** | **5.46+ Million Audit Trail Records** | Immutable JSONB operational telemetry capturing actor, IP, jurisdiction scope, and before/after state transitions. |
| **Sub-100ms Analytics** | **2.11+ Million Pre-Computed Snapshots** | Event-driven PL/pgSQL triggers + non-blocking worker queues guarded by PostgreSQL Advisory Locks, reducing 36-Polda aggregation latency from **>10s to <100ms**. |

### ⚡ Core Architectural Pillars
* **Dual-Node Production Topology**:
  * **Node 1 (Edge Portal & Document Engine)**: Nginx Reverse Proxy (`TLS 1.2/1.3`, HSTS), **Next.js 16.2 + React 19.2** standalone server (**73 App Router pages**, **21 feature bundles**, and offline-first `IndexedDB` preloading **13 temporal partitions**), paired with a Python 3 **Jukminu Polri Document Microservice** (`cas_doc_service.py`) and **ONLYOFFICE Document Server** for real-time collaborative `.docx` drafting.
  * **Node 2 (Core API, Cache, Storage & DB)**: **NestJS 11.1** running **32 PM2 cluster workers** across **26 operational `bdb` submodules** on a 32-core server, backed by **Redis** (`1.5 GB allkeys-lru`), **MinIO S3 Object Storage**, and a dedicated 32-core / 64 GB RAM **PostgreSQL** server.
* **Zero-Trust Security & Hardware MFA**: FIDO2 / WebAuthn Hardware Passkey authentication (`@simplewebauthn/server`), RFC 6238 TOTP 2FA, 6-Digit Security PIN, Proof-of-Work + SVG Captcha, step-up MFA for **Trusted Device Revocation**, and AES-GCM opaque ID encryption.
* **Regulatory & Organizational Precision**: Built in full alignment with **UU No. 27/2022 (UU PDP)**, **Perkap 6/2017 jo. Perpol 4/2025** (supporting all 4 core divisions of Robinopsnal and cleanly separating `INTERNAL_RESERSE` from `EKSTERNAL_RESERSE`), **Perkap 6/2019** (investigation SLA monitoring), and **KUHAP**.

### 🔗 Quick Navigation to Repository Artifacts
* 📘 [**Main Repository (`README.md` / `README.id.md`)**](https://github.com/omeko42/big-data-binops) — Full bilingual system overview & architecture diagrams.
* 📐 [**Architecture Decision Records (`ARCHITECTURE.md`)**](https://github.com/omeko42/big-data-binops/blob/main/ARCHITECTURE.md) — Bilingual ADRs (`ADR-001` through `ADR-005`).
* 🧭 [**Strategic Governance & Platform Evolution (`docs/STRATEGIC_GOVERNANCE_AND_EVOLUTION.md`)**](https://github.com/omeko42/big-data-binops/blob/main/docs/STRATEGIC_GOVERNANCE_AND_EVOLUTION.md) — 4-stage platform evolution, Perpol 4/2025 governance matrix, and 6-pillar roadmap.
* 🖥️ [**Dual-Node Server Inventory (`docs/SERVER_ARCHITECTURE_AND_INVENTORY.md`)**](https://github.com/omeko42/big-data-binops/blob/main/docs/SERVER_ARCHITECTURE_AND_INVENTORY.md) — Production topology, Docker/Nginx/Systemd blueprints, and 26 NestJS submodules.
* 🗄️ [**Live PostgreSQL Schema & Inventory (`database/`)**](https://github.com/omeko42/big-data-binops/tree/main/database) — [`000_live_production_schema.sql`](https://github.com/omeko42/big-data-binops/blob/main/database/schema/000_live_production_schema.sql) (4,878 lines of DDL), [`DATABASE_INVENTORY.md`](https://github.com/omeko42/big-data-binops/blob/main/database/schema/DATABASE_INVENTORY.md), and 90 SQL migrations.
* 🔒 [**Security Policy & Cryptographic Architecture (`SECURITY.md`)**](https://github.com/omeko42/big-data-binops/blob/main/SECURITY.md) — Bilingual security governance & zero-secret verification.

---

## 🛠️ Technology Stack & Engineering Competencies

| Layer | Technologies & Tools |
| :--- | :--- |
| **Languages** | TypeScript 5.7, JavaScript (Node.js 22.14), Python 3, SQL / PL/pgSQL |
| **Backend & Distributed API** | NestJS 11.1.6, TypeORM 0.3.24, Node.js 22.14 (Alpine), PM2 Cluster (32 workers), `@simplewebauthn/server` (FIDO2), Passport JWT, `otplib` (TOTP), Puppeteer + `qpdf`, ExcelJS, `pdfmake` |
| **Frontend & Web Client** | Next.js 16.2.10 (App Router, Standalone), React 19.2.4, PrimeReact 10.9.8, Chart.js 4.5.1, Lucide React, Axios, Offline-First IndexedDB (`bdb_offline_db`) |
| **Document Automation** | Python 3 `ThreadingHTTPServer` (`cas_doc_service.py` — Jukminu Polri Engine), ONLYOFFICE Document Server (`onlyoffice-ds`), SQLite |
| **Database & Caching** | PostgreSQL 15/16 (171 tables, 433 indexes, `pg_trgm`, Advisory Locks, custom PL/pgSQL triggers), Redis (`redis:alpine`, `ioredis`, `@keyv/redis` — 1.5 GB `allkeys-lru`) |
| **Infrastructure & DevOps** | MinIO S3 Object Storage, Nginx Reverse Proxy (TLS 1.2/1.3, HSTS), Docker & Docker Compose, Systemd, Linux Crontab |

---

<div align="center">
  <b>Eko Agung (`@omeko42`)</b><br/>
  <i>Full-Stack Software Engineer & System Architect • Founder of CAS (Community Anggota Serse) & Lead Architect of Big Data Binops (BDB)</i>
</div>
