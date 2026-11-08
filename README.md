# KWN_Revamp

[![CI/CD Pipeline](https://github.com/hastura/KWN_Revamp/actions/workflows/ci-cd.yml/badge.svg)](https://github.com/hastura/KWN_Revamp/actions/workflows/ci-cd.yml)

Website revamp & prototype interaktif untuk **Kreasi Warna Nusantara (KWN)** — Solusi Desain & Build Booth Exhibition dan Event Organizer di Jakarta Timur.

## 🚀 Live Demo
- **Live Prototype (End-User Website)**: [https://hastura.github.io/KWN_Revamp/](https://hastura.github.io/KWN_Revamp/)
- **CMS Content Studio (Admin Prototype)**: [https://hastura.github.io/KWN_Revamp/KWN%20Prototype/kwn-cms.html](https://hastura.github.io/KWN_Revamp/KWN%20Prototype/kwn-cms.html)
- **Editorial Version**: [https://hastura.github.io/KWN_Revamp/KWN%20Editorial/kwn-editorial.html](https://hastura.github.io/KWN_Revamp/KWN%20Editorial/kwn-editorial.html)

---

## 📂 Struktur Repositori

```text
KWN_Revamp/
├── .github/workflows/
│   └── ci-cd.yml             # GitHub Actions CI/CD Pipeline
├── KWN Prototype/
│   ├── kwn-prototype.html    # Prototype End-User: Editorial structure + Navy Glassmorphism
│   └── kwn-cms.html          # Prototype CMS: KWN Content Studio (Home, Rental & Edit)
├── KWN Editorial/
│   └── kwn-editorial.html    # Layout editorial awal
├── KWN Glassmorphism/        # Aset & referensi visual mockup navy glassmorphism
├── KWN Classy Style/         # Referensi gaya classy style
├── index.html                # Entry point portal & redirect
└── README.md
```

---

## 🛠️ Fitur Prototype Utama

- **Seamless Switcher (End-User ⇄ CMS)**: Tombol mengambang (*floating pill*) dan tautan navbar pada kedua interface untuk beralih instan antara tampilan pengunjung (*End-User Website*) dan panel pengelolaan konten (*CMS Content Studio*).
- **KWN Content Studio (CMS)**:
  - **Home Content View**: Pengaturan urutan seksi hero, toggle aktif/nonaktif seksi, live preview card secara real-time, dan audit riwayat perubahan.
  - **Furniture Rent View (Aset Sewa)**: Tabel aset sewa interaktif dengan pencarian, filter kategori (*Properti, Furniture, Sign Box*), status ketersediaan, dan toggle tayang di website.
  - **Edit Aset View**: Form edit nama aset, kategori, deskripsi, upload foto cover, live preview pesan WhatsApp otomatis, dan preview baris katalog website.
- **3D Frosted Glass Rotating Cube Hero**: Kubus 3D kaca interaktif dengan inersia rotasi, indikator menu per sisi (*About, Our Project, Furniture Rent, Contact, KWN Monogram*), dan navigasi klik langsung.
- **Floating Glass Navigation Bar**: Navigasi mengambang bertepi rounded dengan efek blur dan responsive drawer mobile.
- **Hero Process Mini-Cards**: Strip proses kaca 4 langkah (*01 Konsultasi, 02 Desain, 03 Produksi, 04 Event Jalan*).
- **Core Business & Services**: Penjelasan dua pilar utama (*Design and Build* & *Event Organizer*).
- **Clients Marquee**: Strip kaca horizontal dengan running marquee nama-nama klien besar.
- **Project Showcase**: Grid karya terbaru dengan visual gradien dan efek hover zoom.
- **Furniture Rent Catalogue**: Halaman katalog sewa interaktif dengan transisi tirai (*curtain page transition*), filter tab (*Properti, Furniture, Sign Box*), dan integrasi langsung WhatsApp.

---

## 🔄 CI/CD Pipeline

Pipeline otomatis dikelola melalui **GitHub Actions** ([`.github/workflows/ci-cd.yml`](.github/workflows/ci-cd.yml)):

1. **Continuous Integration (CI)**:
   - Validasi struktur direktori dan keberadaan file inti.
   - Linting sintaks HTML dengan `htmlhint`.
   - Dijalankan pada setiap `push` dan `pull_request` ke branch `main`.

2. **Continuous Deployment (CD)**:
   - Membundel seluruh prototype dan aset ke dalam `_site/`.
   - Menetapkan prototype utama sebagai `index.html` root.
   - Otomatis deploy ke **GitHub Pages** menggunakan `actions/deploy-pages@v4`.
