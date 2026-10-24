# Eko Agung (`@omeko42`)
### Full-Stack Software Engineer & System Architect
*Founder of **CAS (Community Anggota Serse — 1,024+ Members)** & Lead Architect of **Big Data Binops (BDB)***

[![Platform](https://img.shields.io/badge/Flagship%20System-Big%20Data%20Binops%20(BDB)%20v2.5-1E40AF.svg?style=flat-square)](https://github.com/omeko42/big-data-binops)
[![Community](https://img.shields.io/badge/Community-CAS%20(1,024%2B%20Active%20Members)-25D366.svg?style=flat-square&logo=whatsapp&logoColor=white)](https://github.com/omeko42/big-data-binops)
[![Scale](https://img.shields.io/badge/Production%20DB-68.89M%2B%20Rows%20%7C%20171%20Tables-336791.svg?style=flat-square&logo=postgresql&logoColor=white)](https://github.com/omeko42/big-data-binops/blob/main/database/schema/DATABASE_INVENTORY.md)
[![Latency](https://img.shields.io/badge/Analytical%20Latency-%3C100ms%20(Snapshot%20Engine)-10B981.svg?style=flat-square)](https://github.com/omeko42/big-data-binops/blob/main/ARCHITECTURE.md)

---

## 👋 Executive Profile

I am a **Data Analyst turned Full-Stack Engineer and System Architect** specializing in high-scale operational data governance, distributed relational database engineering, and zero-trust enterprise web systems.

At **Biro Pembinaan dan Operasional (Robinopsnal) Bareskrim Polri**, I lived through four evolutionary stages of national law enforcement data management — from fragmented regional Excel templates and a 34-day `15.02 GB` public cloud quota lock (`153+` exploding spreadsheet tabs), to a third-party legacy system failure. To solve these structural bottlenecks permanently, I founded **CAS (*Community Anggota Serse*)** — uniting **1,024+ active criminal investigation personnel, operators, Kanit Reskrim, and Kaur Binops (KBO)** across Indonesia — and architected **Big Data Binops (BDB)** from the ground up.

---

## 🏛️ Flagship Architectural Case Study: [Big Data Binops (BDB) — Powered by CAS](https://github.com/omeko42/big-data-binops)

[**`omeko42/big-data-binops`**](https://github.com/omeko42/big-data-binops) is an enterprise-grade operational data governance, 4-tier case lifecycle management, and sub-100ms analytics platform operating across **Mabes Polri $\to$ 36 Polda $\to$ 508+ Polres $\to$ 4,900+ Polsek**.

### 📊 Verified Production Scale (PostgreSQL 15 Live Inventory)
| Metric / Domain | Verified Production Scale | Architectural Implementation |
| :--- | :--- | :--- |
| **Total Active Database Rows** | **`~68,890,877` (`~68.89M` rows)** | Distributed across **171 active tables**, **1 SQL View**, **2,283 columns**, **496 constraints**, **433 indexes** (`B-Tree`, `GIN pg_trgm`), **7 PL/pgSQL functions**, **5 triggers**, and **90 SQL migrations**. |
| **Core Police Reports (LP)** | **`2,852,128` raw / `2,847,302` normalized** | Decoupled immutable JSONB staging (`bdb_dors_raw_lp`) $\to$ normalized core (`bdb_laporan_polisi`) with `REGEXP_REPLACE` NBSP (`chr(160)`) sanitization across **14,217 Satker nodes**. |
| **Involved Parties & Syndicates** | **`11,164,838` party records** | National NIK/NRP/Corporate entity resolution (`bdb_dors_lp_terlibat`) & cross-province syndicate scoring (`bdb_pihak_terlibat_ranking_snapshot` — **5,828 multi-Polda subjects**). |
| **National Evidence Registry** | **`5,840,308` evidence items** | Normalized DORS evidence (`bdb_dors_lp_barang_bukti`) + manual investigator seizures (`bdb_lp_barang_bukti_manual`) & pre-computed summary snapshots (**171,595 rows**). |
| **Forensic Audit Trail** | **`5,469,632` live audit logs** | Immutable JSONB telemetry (`bdb_audit_log`) capturing User ID, IP, Action, Entity, and Metadata across all law enforcement operations. |
| **Pre-Computed Snapshot Engine** | **`2,114,283` LP snapshot rows** | Real-time trigger (`bdb_trg_sync_kinerja_snapshot_from_lp`) + non-blocking `setImmediate()` workers guarded by PostgreSQL Advisory Locks, cutting national aggregation queries from **`>10s` to `<100ms`**. |

### ⚡ Key Architectural Highlights
* **Dual-Node Production Cluster**:
  * **Node 1 (Edge / Portal & Docs)**: Nginx Reverse Proxy (`TLS 1.2/1.3`, HSTS), Next.js `16.2.10` + React `19.2.4` standalone server (**73 App Router pages**, **21 feature bundles**, custom `Cache-Control` hotfix guard, and offline-first `IndexedDB` preloading **13 temporal partitions**), plus a Python 3 **Jukminu Polri Document Microservice** (`cas_doc_service.py` on port `3860`) integrated with **ONLYOFFICE Document Server** (`onlyoffice-ds` on port `8088`) and an in-browser **13-Sheet Official Perkap Polri WYSIWYG Suite**.
  * **Node 2 (Core / API, Storage & DB)**: NestJS `11.1.6` (`node:22.14.0-alpine` with Headless Chromium + `qpdf`) running **32 PM2 cluster worker instances** across **26 operational `bdb` submodules** on a 32-core server, paired with Redis (`1.5 GB allkeys-lru`), MinIO S3 Object Storage (`bdb-attachments` via a **Dual-Client Pattern**), and a dedicated 32-core / 64 GB RAM PostgreSQL server (`max_connections = 300`).
* **FIDO2 / WebAuthn Hardware Passkey & Zero-Trust Security**: Hardware-bound biometric authentication (`@simplewebauthn/server` with mandatory `userVerification: 'required'`), RFC 6238 TOTP 2FA, 6-Digit Security PIN, PoW + SVG Captcha, Email OTP, step-up MFA for **Trusted Device Revocation**, cross-tab session termination (`BroadcastChannel`), and AES-GCM opaque ID ciphers (`id-cipher.util.ts`).
* **Full Regulatory & SOTK Alignment**: Engineered in strict compliance with **UU No. 27/2022 (UU PDP)**, **Perkap 6/2017 jo. Perpol 4/2025** (unifying *Bagrenopsnal*, *Bagkerma*, *Baganev*, and *Bagyanmas*, and isolating `INTERNAL_RESERSE` from `EKSTERNAL_RESERSE`), **Perkap 6/2019** (30d–120d investigation SLA engine), and **KUHAP** (enforcing the juridical doctrine that **P-21** remains active CT workload until physical **Tahap II** handover).
* **Proven Mathematical Reconciliation (2026 Benchmarks)**: Resolved an urgent `8 LP` cross-source delta (`1,728` raw DORS vs `1,720` Directorate recap) in minutes during executive diplomatic preparation, and passed a **100% verified 36-Polda mathematical audit** across **`270,059 CT` nationally** (`269,436 CT` across 36 Polda + `623 CT` Bareskrim).

### 🔗 Direct Repository Deep-Dive Links
* 📐 [**Architecture Decision Records (`ARCHITECTURE.md`)**](https://github.com/omeko42/big-data-binops/blob/main/ARCHITECTURE.md) — Bilingual ADRs (`ADR-001` through `ADR-005`).
* 🧭 [**Strategic Governance & 4-Stage Evolution (`docs/STRATEGIC_GOVERNANCE_AND_EVOLUTION.md`)**](https://github.com/omeko42/big-data-binops/blob/main/docs/STRATEGIC_GOVERNANCE_AND_EVOLUTION.md) — Empirical history, SOTK Perpol 4/2025 matrix, and 6-Pillar Blueprint.
* 🖥️ [**Dual-Node Server Architecture & Inventory (`docs/SERVER_ARCHITECTURE_AND_INVENTORY.md`)**](https://github.com/omeko42/big-data-binops/blob/main/docs/SERVER_ARCHITECTURE_AND_INVENTORY.md) — Forensic topology of Node 1 & Node 2, ports, crons, and 26 NestJS submodules.
* 🗄️ [**Database Schema & 68.89M-Row Inventory (`database/`)**](https://github.com/omeko42/big-data-binops/tree/main/database) — Live DDL ([`000_live_production_schema.sql`](https://github.com/omeko42/big-data-binops/blob/main/database/schema/000_live_production_schema.sql)), [`DATABASE_INVENTORY.md`](https://github.com/omeko42/big-data-binops/blob/main/database/schema/DATABASE_INVENTORY.md), and 90 sequential migrations.
* ⚙️ [**Backend NestJS 11 Cluster Mirror (`backend/`)**](https://github.com/omeko42/big-data-binops/tree/main/backend) — `app_core`, 26 `bdb` submodules, `external` API gateway, `Dockerfile.bdb`, and 32-worker `ecosystem.config.js`.
* 🌐 [**Frontend Next.js 16.2 Portal & Python Jukminu Service (`frontend/`)**](https://github.com/omeko42/big-data-binops/tree/main/frontend) — [`FRONTEND_ROUTES_AND_MODULES.md`](https://github.com/omeko42/big-data-binops/blob/main/frontend/FRONTEND_ROUTES_AND_MODULES.md) (73 App Router pages, 21 bundles) and [`cas_doc_service.py`](https://github.com/omeko42/big-data-binops/blob/main/frontend/services/cas-doc-service/cas_doc_service.py).
* 🔒 [**Security Policy & Cryptographic Architecture (`SECURITY.md`)**](https://github.com/omeko42/big-data-binops/blob/main/SECURITY.md) — FIDO2 WebAuthn, Zero-Secret hygiene, and UU PDP compliance.

---

## 🛠️ Verified Technology Stack

| Layer | Technologies Used in Production |
| :--- | :--- |
| **Languages** | TypeScript 5.7, JavaScript (Node.js 22.14), Python 3, SQL / PL/pgSQL |
| **Backend & API** | NestJS 11.1.6, TypeORM 0.3.24, Node.js 22.14 (Alpine), PM2 Cluster (32 workers), `@simplewebauthn/server` (FIDO2), Passport JWT, `otplib` (TOTP), Puppeteer + `qpdf`, ExcelJS, `pdfmake`, Autocannon |
| **Frontend & Client** | Next.js 16.2.10 (App Router, Standalone), React 19.2.4, PrimeReact 10.9.8, Chart.js 4.5.1, Lucide React 1.24.0, Axios 1.18.1, Offline-First IndexedDB (`bdb_offline_db`) |
| **Document Engine** | Python 3 `ThreadingHTTPServer` (`cas_doc_service.py` — Jukminu Polri Engine), ONLYOFFICE Document Server (`onlyoffice-ds`), SQLite |
| **Database & Caching** | PostgreSQL 15/16 (171 tables, 433 indexes, `pg_trgm`, Advisory Locks, customPL/pgSQL triggers), Redis (`redis:alpine`, `ioredis`, `@keyv/redis` — 1.5 GB `allkeys-lru`) |
| **Storage & DevOps** | MinIO S3 Object Storage (`bdb-attachments`), Nginx Reverse Proxy (TLS 1.2/1.3, HSTS), Docker & Docker Compose, Systemd, Linux Crontab |
