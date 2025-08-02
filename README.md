# Sistem Informasi Perpustakaan Digital

Aplikasi web sederhana berbasis Laravel dan Bootstrap untuk mengelola data perpustakaan seperti buku, anggota, dan peminjaman. Sistem mendukung tiga jenis pengguna: Admin, Pustakawan, dan User, dengan hak akses yang berbeda.

## 🎯 Fitur Utama

- Autentikasi dan otorisasi pengguna (Admin, Pustakawan, User)
- CRUD data Buku dan Anggota
- Pencarian dan filter daftar buku
- Upload gambar sampul buku
- Tampilan responsif dengan Bootstrap
- Validasi data
- Role-based dashboard
- Export data ke PDF *(opsional)*

## 👥 Role & Akses

| Role        | Akses                                         |
|-------------|-----------------------------------------------|
| Admin       | Pustakawan                                    |
| Pustakawan  | Buku, peminjaman, member                      |
| User        | Lihat daftar buku dan status peminjaman       |

### Akun Default:

| Role        | Username               | Password   |
|-------------|------------------------|------------|
| Admin       | `6969`                 | `password` |
| Pustakawan  | `9999`                 | `password` |
| User        | `9696`, `270103`       | `password` |

## ⚙️ Teknologi

- **Backend:** Laravel 11
- **Frontend:** Blade, Bootstrap 5
- **Database:** MySQL
- **Authentication:** Laravel Auth
- **Optional:** Vue.js, PDF Export, Pagination

## 🚀 Cara Menjalankan Proyek

1. **Clone repository ini:**
   ```bash
   git clone https://github.com/username/perpustakaan-laravel.git
   cd perpustakaan-laravel
Install dependensi:

bash
Salin
Edit
composer install
npm install && npm run dev
Salin file environment dan konfigurasi database:

bash
Salin
Edit
cp .env.example .env
php artisan key:generate
Atur koneksi database di .env:

env
Salin
Edit
DB_DATABASE=perpustakaan_db
DB_USERNAME=root
DB_PASSWORD=
Jalankan migrasi dan seeder (optional untuk akun default):

bash
Salin
Edit
php artisan migrate --seed
Jalankan aplikasi:

bash
Salin
Edit
php artisan serve
Akses di browser:

arduino
Salin
Edit
http://localhost:8000
📁 Struktur Folder Utama
swift
Salin
Edit
├── app/Http/Controllers/
│   ├── AuthController.php
│   ├── BukuController.php
│   └── AnggotaController.php
├── resources/views/
│   ├── layouts/
│   ├── buku/
│   ├── anggota/
│   └── auth/
└── public/assets/
    ├── css/
    └── js/