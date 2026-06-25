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
- Membuat halaman login.
Mengatur perpindahan halaman/menu.
Membuat dashboard dan tampilan utama aplikasi.
Mengatur desain (style) aplikasi.

### Aditia Rahmat Maulana (F1D02310030)
- CRUD data produk (tambah, edit, hapus, cari).
CRUD data user/kasir.
Membuat dan menghubungkan database.
Mengelola tabel dan query database.

### Amalia Mirasafitri (F1D02310002)
- Membuat fitur transaksi/POS.
Menghitung total pembayaran.
Menampilkan riwayat transaksi.
Membuat laporan dan fitur export data.

---

## Screenshot
- Berada di folder ss
---
