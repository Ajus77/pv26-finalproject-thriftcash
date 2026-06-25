# ThriftCash 👕
**Sistem Kasir Desktop untuk Toko Pakaian Bekas (Thrift Shop)**

> Final Project — Pemrograman Visual (PySide6) | Semester Genap 2025/2026

---

## Deskripsi Aplikasi
ThriftCash adalah aplikasi kasir desktop yang dirancang khusus untuk kebutuhan operasional toko pakaian bekas (*thrift shop*). Aplikasi ini mempermudah kasir dalam mengelola produk, memproses transaksi penjualan secara real-time, serta memantau laporan pendapatan harian maupun mingguan.
Latar belakang pemilihan topik ini karena bisnis thrift shop berkembang pesat namun banyak yang masih mengandalkan pencatatan manual. ThriftCash hadir sebagai solusi pencatatan yang cepat, akurat, dan terdokumentasi dengan baik.

---

## Anggota Kelompok
| Nama | NIM | 
|------|-----|
| Amalia Mirasafitri | F1D02310002 | 
| Bagus Esa Wijaya Kusuma | F1D02310005 | 
| Aditia Rahmat Maulana | F1D02310030 | 

---

## Fitur Utama
- **Login & Manajemen Sesi** — Autentikasi pengguna dengan role *admin* dan *kasir*, disertai logout dengan konfirmasi
- **Dashboard** — Ringkasan transaksi dan pendapatan hari ini, grafik bar pendapatan 7 hari, dan pie chart distribusi penjualan per kategori. Auto-refresh setiap 30 detik
- **Kasir / POS** — Tambah produk ke keranjang, atur diskon, hitung kembalian otomatis, dan simpan transaksi lengkap dengan nomor invoice otomatis
- **Manajemen Produk** — CRUD produk dengan pencarian real-time, filter kategori, sorting multi-kolom, dan indikator warna untuk stok menipis
- **Laporan Transaksi** — Riwayat transaksi dengan filter tanggal dan pencarian, detail per invoice melalui double-klik
- **Export Data** — Export ke CSV dan PDF (ReportLab) untuk laporan transaksi, serta export CSV untuk daftar produk
- **Manajemen Pengguna** — CRUD pengguna khusus admin, dengan proteksi agar admin tidak bisa menghapus akunnya sendiri

---

## Cara Menjalankan
### 1. Clone repository
```bash
git clone https://github.com/[Ajus77]/pv26-finalproject-thriftcash.git
cd pv26-finalproject-thriftcash
```

### 2. Install dependensi
```bash
pip install -r requirements.txt
```

### 3. Jalankan aplikasi
```bash
python main.py
```

> Database `thriftcash.db` akan otomatis terbuat beserta data awal (admin dan 10 produk sample) saat pertama kali dijalankan.

### 4. Login default
| Field | Value |
|-------|-------|
| Username | `admin` |
| Password | `admin123` |

---

## Struktur Folder
```
pv26-finalproject-thriftcash/
├── main.py              — Entry point aplikasi
├── requirements.txt     — Daftar dependensi
├── README.md
├── .gitignore
├── assets/
│   └── style.qss        — Stylesheet global (QSS)
├── database/
│   └── db.py            — Inisialisasi schema & seluruh query SQLite
├── ui/
│   ├── login_window.py  — Halaman login
│   ├── main_window.py   — Jendela utama (sidebar + navigasi)
│   ├── dashboard_page.py — Halaman dashboard & chart
│   ├── pos_page.py      — Halaman kasir / POS
│   ├── product_page.py  — Halaman manajemen produk
│   ├── report_page.py   — Halaman laporan transaksi
│   └── user_page.py     — Halaman manajemen pengguna
└── utils/
    └── export.py        — Helper export CSV, PDF, dan struk .txt
```

---

## Pembagian Tugas
### Bagus Esa Wijaya Kusuma (F1D02310005)
- `ui/login_window.py` — Form login dengan validasi dan signal autentikasi
- `ui/dashboard_page.py` — Stat cards, bar chart pendapatan 7 hari, pie chart per kategori, auto-refresh
- `main.py` — Entry point, inisialisasi app, alur login–logout
- `assets/style.qss` (baris 101–235) — Styling stat card, tombol, input form, dan label

### Aditia Rahmat Maulana (F1D02310030)
- `ui/product_page.py` — Tabel produk, dialog tambah/edit, search real-time, filter, sorting, indikator stok
- `ui/user_page.py` — Tabel pengguna, dialog tambah/edit, proteksi hapus akun sendiri
- `database/db.py` — Schema 4 tabel, relasi FK, seluruh fungsi CRUD dan analitik dashboard
- `assets/style.qss` (baris 1–100 + 287–316) — Styling global, sidebar, topbar, dan komponen POS

### Amalia Mirasafitri (F1D02310002)
- `ui/pos_page.py` — Tabel produk, keranjang belanja, diskon, dialog pembayaran, simpan transaksi
- `ui/report_page.py` — Tabel transaksi, filter tanggal, summary strip, dialog detail invoice
- `utils/export.py` — Fungsi export CSV transaksi, CSV produk, PDF via ReportLab, dan struk .txt
- `assets/style.qss` (baris 165–286 + 317–362) — Styling tabel, menu bar, scrollbar, dialog, login card, badges

---

## Screenshot
Berada di file ss
---
