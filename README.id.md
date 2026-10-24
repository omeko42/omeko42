<div align="right">
  <b>🌐 Bahasa / Language:</b> &nbsp;
  <a href="https://github.com/omeko42/omeko42/blob/main/README.md">🇬🇧 English</a> &nbsp;|&nbsp;
  <a href="https://github.com/omeko42/omeko42/blob/main/README.id.md"><b>🇮🇩 Bahasa Indonesia (Aktif)</b></a>
</div>

# Eko Agung (`@omeko42`)
### Full-Stack Software Engineer & System Architect
*Pendiri **CAS (Community Anggota Serse — 1.024+ Anggota)** & Arsitek Utama **Big Data Binops (BDB)***

[![Flagship Platform](https://img.shields.io/badge/Platform%20Utama-Big%20Data%20Binops%20(BDB)%20v2.5-1E40AF.svg?style=flat-square)](https://github.com/omeko42/big-data-binops/blob/main/README.id.md)
[![Community](https://img.shields.io/badge/Komunitas-CAS%20(1.024%2B%20Anggota%20Aktif)-25D366.svg?style=flat-square&logo=whatsapp&logoColor=white)](https://github.com/omeko42/big-data-binops/blob/main/README.id.md)
[![Production Scale](https://img.shields.io/badge/DB%20Produksi-68,89%20Juta%2B%20Baris%20%7C%20171%20Tabel-336791.svg?style=flat-square&logo=postgresql&logoColor=white)](https://github.com/omeko42/big-data-binops/blob/main/database/schema/DATABASE_INVENTORY.md)
[![Analytical Latency](https://img.shields.io/badge/Latensi%20Analitik-%3C100ms%20(Mesin%20Snapshot)-10B981.svg?style=flat-square)](https://github.com/omeko42/big-data-binops/blob/main/ARCHITECTURE.md)
[![Security & License](https://img.shields.io/badge/Lisensi%20%7C%20NDA%20%7C%20SLA-FIDO2%20WebAuthn%20%2B%20Zero--Trust-059669.svg?style=flat-square)](https://github.com/omeko42/big-data-binops/blob/main/LICENSE.md)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Eko%20Agung%20(%40omeko42)-0A66C2.svg?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/omeko42/)

---

## 👋 Profil Eksekutif

Saya adalah seorang **Analis Data Operasional yang bertransformasi menjadi Full-Stack Software Engineer dan System Architect**, dengan spesialisasi pada tata kelola data operasional berskala besar, rekayasa basis data relasional terdistribusi, serta sistem web *enterprise* berbasis *zero-trust*.

Berangkat dari pengalaman langsung mengelola dan menganalisis data operasional nasional di lingkungan **Biro Pembinaan dan Operasional (Robinopsnal) Bareskrim Polri**, saya memahami secara nyata kompleksitas rekonsiliasi jutaan rekaman data penegakan hukum di seluruh Indonesia. Untuk menyelesaikan tantangan struktural tersebut secara permanen dari hulu ke hilir, saya mengambil dua langkah utama:

1. **Mendirikan CAS (*Community Anggota Serse*)**: Membangun gerakan dan komunitas operasional organik dari bawah ke atas (*bottom-up*) yang menghimpun **1.024+ penyidik aktif, operator, Kanit Reskrim Polsek, hingga Kaur Binops (KBO)** se-Indonesia melalui grup komunikasi taktis WhatsApp dan forum internal **SHARESE** — menciptakan lingkar umpan balik (*feedback loop*) langsung antara petugas lapangan dan pengembangan sistem.
2. **Merancang & Membangun Big Data Binops (BDB)**: Merekayasa platform tata kelola data operasional berdaulat dari nol — mengonsolidasikan data majemuk lintas sumber tanpa beban pengisian ganda (*bebas dobel input*), serta menghadirkan analitik kinerja nasional berkecepatan di bawah **100 milidetik** di seluruh 4 tingkatan kewilayahan (**Mabes Polri → 36 Polda → 508+ Polres → 4.900+ Polsek**).

---

## 🏛️ Portofolio Rekayasa Utama: [Big Data Binops (BDB) — Powered by CAS (Community Anggota Serse)](https://github.com/omeko42/big-data-binops/blob/main/README.id.md)

[**`omeko42/big-data-binops`**](https://github.com/omeko42/big-data-binops/blob/main/README.id.md) adalah platform tata kelola data operasional, manajemen siklus hidup perkara 4 tingkat kewilayahan, serta otomatisasi naskah dinas penegakan hukum (**🇮🇩 [Dokumentasi Bahasa Indonesia](https://github.com/omeko42/big-data-binops/blob/main/README.id.md)** | **🇬🇧 [English Documentation](https://github.com/omeko42/big-data-binops/blob/main/README.md)**).

### 📊 Skala Produksi Terverifikasi
| Domain Operasional | Skala Produksi Aktual | Sorotan Rekayasa Arsitektur |
| :--- | :--- | :--- |
| **Skala Basis Data** | **~68,89 Juta Baris Aktif** | **171 tabel PostgreSQL aktif**, **433 indeks** (`B-Tree`, `GIN pg_trgm`), **7 fungsi PL/pgSQL**, **5 trigger real-time**, dan **90 migrasi SQL berurutan**. |
| **Siklus Hidup Perkara (LP)** | **2,84+ Juta Laporan Polisi** | Sinkronisasi otomatis dari **DORS Stamaops Polri (Staf Utama Kapolri Bidang Operasi)** ke *staging* JSONB *immutable* → tabel inti ternormalisasi di **14.217 simpul Satker**. |
| **Graf Pihak & Barang Bukti** | **11,16 Juta+ Pihak & 5,84 Juta+ Barang Bukti** | Resolusi entitas NIK/NRP/Korporasi lintas provinsi, pemeringkatan jaringan sindikat lintas Polda, dan pelacakan barang bukti ganda. |
| **Jejak Audit Forensik** | **5,46+ Juta Catatan Audit** | Telemetri operasional JSONB *immutable* yang mencatat aktor, IP, cakupan yurisdiksi, dan perubahan status sebelum/sesudah secara presisi. |
| **Analitik Sub-100ms** | **2,11+ Juta Baris Snapshot Pra-Hitung** | Trigger PL/pgSQL *real-time* + antrean *worker* non-blocking dengan PostgreSQL Advisory Locks, memangkas waktu agregasi 36 Polda dari **>10 detik menjadi <100ms**. |

### ⚡ Pilar Arsitektur Utama
* **Topologi Produksi Dual-Node**:
  * **Node 1 (Edge Portal & Mesin Dokumen)**: Nginx Reverse Proxy (`TLS 1.2/1.3`, HSTS), server mandiri **Next.js 16.2 + React 19.2** (**73 halaman App Router**, **21 bundel fitur**, dan penyimpanan lokal `IndexedDB` *offline-first* **13 partisi waktu**), dipadukan dengan **Layanan Mikro Dokumen Jukminu Polri** berbasis Python 3 (`cas_doc_service.py`) serta **ONLYOFFICE Document Server** untuk penyusunan draf `.docx` kolaboratif.
  * **Node 2 (Core API, Cache, Storage & DB)**: **NestJS 11.1** yang menjalankan **32 *worker instance* PM2 Cluster** pada **26 sub-modul operasional `bdb`** di server 32-core, didukung oleh **Redis** (`1.5 GB allkeys-lru`), **MinIO S3 Object Storage**, dan server khusus **PostgreSQL** (32-core / 64 GB RAM).
* **Keamanan Zero-Trust & MFA Perangkat Keras**: Autentikasi biometrik perangkat keras FIDO2 / WebAuthn Passkey (`@simplewebauthn/server`), TOTP 2FA (RFC 6238), PIN Keamanan 6 Digit, PoW + SVG Captcha, otorisasi MFA bertingkat untuk **Cabut Akses Gawai Terpercaya**, serta enkripsi ID buram AES-GCM.
* **Kepatuhan Regulasi & SOTK Polri**: Dirancang selaras penuh dengan **UU No. 27 Tahun 2022 (UU PDP)**, **Perkap 6/2017 jo. Perpol 4/2025** (mengakomodasi 4 Bagian inti Robinopsnal serta memisahkan kamar `INTERNAL_RESERSE` dari `EKSTERNAL_RESERSE`), **Perkap 6/2019** (pemantauan SLA penyidikan), dan **KUHAP**.

### 🔗 Tautan Cepat ke Dokumentasi Repositori
* 📘 [**Halaman Utama Repositori (`README.id.md` / `README.md`)**](https://github.com/omeko42/big-data-binops/blob/main/README.id.md) — Ikhtisar sistem lengkap & diagram arsitektur dwibahasa.
* 📐 [**Catatan Keputusan Arsitektur (`ARCHITECTURE.md`)**](https://github.com/omeko42/big-data-binops/blob/main/ARCHITECTURE.md) — Dokumen ADR dwibahasa (`ADR-001` s/d `ADR-005`).
* 🧭 [**Telaahan Strategis & Evolusi Platform (`docs/STRATEGIC_GOVERNANCE_AND_EVOLUTION.md`)**](https://github.com/omeko42/big-data-binops/blob/main/docs/STRATEGIC_GOVERNANCE_AND_EVOLUTION.md) — Evolusi 4 tahap, matriks SOTK Perpol 4/2025, dan cetak biru 6 pilar.
* 🖥️ [**Inventaris & Topologi Server Dual-Node (`docs/SERVER_ARCHITECTURE_AND_INVENTORY.md`)**](https://github.com/omeko42/big-data-binops/blob/main/docs/SERVER_ARCHITECTURE_AND_INVENTORY.md) — Topologi produksi, konfigurasi Docker/Nginx/Systemd, dan 26 sub-modul NestJS.
* 🗄️ [**Skema PostgreSQL Produksi & Inventaris 68,89 Juta Baris (`database/`)**](https://github.com/omeko42/big-data-binops/tree/main/database) — [`000_live_production_schema.sql`](https://github.com/omeko42/big-data-binops/blob/main/database/schema/000_live_production_schema.sql) (4.878 baris DDL), [`DATABASE_INVENTORY.md`](https://github.com/omeko42/big-data-binops/blob/main/database/schema/DATABASE_INVENTORY.md), dan 90 migrasi SQL.
* ⚖️ [**Lisensi Kedinasan, NDA, SLA & Kebijakan Keamanan (`LICENSE.md`)**](https://github.com/omeko42/big-data-binops/blob/main/LICENSE.md) — Tata kelola lisensi, kerahasiaan NDA, SLA 99,9% & kriptografi dwibahasa.

---

## 🛠️ Tumpukan Teknologi (*Technology Stack*)

| Lapisan | Teknologi & Instrumen Produksi |
| :--- | :--- |
| **Bahasa Pemrograman** | TypeScript 5.7, JavaScript (Node.js 22.14), Python 3, SQL / PL/pgSQL |
| **Backend & API Terdistribusi** | NestJS 11.1.6, TypeORM 0.3.24, Node.js 22.14 (Alpine), PM2 Cluster (32 workers), `@simplewebauthn/server` (FIDO2), Passport JWT, `otplib` (TOTP), Puppeteer + `qpdf`, ExcelJS, `pdfmake` |
| **Frontend & Klien Web** | Next.js 16.2.10 (App Router, Standalone), React 19.2.4, PrimeReact 10.9.8, Chart.js 4.5.1, Lucide React, Axios, Offline-First IndexedDB (`bdb_offline_db`) |
| **Otomatisasi Dokumen** | Python 3 `ThreadingHTTPServer` (`cas_doc_service.py` — Mesin Jukminu Polri), ONLYOFFICE Document Server (`onlyoffice-ds`), SQLite |
| **Basis Data & Caching** | PostgreSQL 15/16 (171 tabel, 433 indeks, `pg_trgm`, Advisory Locks, custom PL/pgSQL triggers), Redis (`redis:alpine`, `ioredis`, `@keyv/redis` — 1.5 GB `allkeys-lru`) |
| **Infrastruktur & DevOps** | MinIO S3 Object Storage, Nginx Reverse Proxy (TLS 1.2/1.3, HSTS), Docker & Docker Compose, Systemd, Linux Crontab |

---

<div align="center">
  <b>Eko Agung (`@omeko42`)</b> — <a href="https://github.com/omeko42">GitHub</a> &nbsp;|&nbsp; <a href="https://www.linkedin.com/in/omeko42/">LinkedIn</a><br/>
  <i>Full-Stack Software Engineer & System Architect • Pendiri CAS (Community Anggota Serse) & Arsitek Utama Big Data Binops (BDB)</i>
</div>
