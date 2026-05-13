# Setup PHP dan Laravel

Cek Versi:

```sh
    php -v
    composer -V
```

---

## 1. Buat Project Laravel

```sh
composer create-project laravel/laravel myapp
```

---

## 2. Masuk ke Folder Project

```sh
cd myapp
```

---

## 3. Jalankan Laravel

```sh
php artisan serve
```

Buka browser:

```sh
http://127.0.0.1:8000
```

---

## 4. Setup Database

Buka file `.env` dan sesuaikan konfigurasi:

```sh
DB_DATABASE=laravel_db
DB_USERNAME=root
DB_PASSWORD=
```

Pastikan database sudah dibuat di `phpMyAdmin`

## 6. Struktur yang wajib

```sh
myapp/
├── app/
│   ├── Http/
│   │    └── Controllers/    → Tempat logic aplikasi (SAW, perhitungan, dashboard, dll)
│   └── Models/
├── bootstrap/
├── config/
├── database/
├── public/
├── resources/
│   └── views/              → Tampilan (Blade template: UI, halaman web)
├── routes/
│   └── web.php             → Mengatur URL / routing aplikasi
├── storage/
├── tests/
├── vendor/
├── .env                    → Konfigurasi aplikasi (database, app name, mode, dll)
│
...
```

---

## 7 Laravel Artisan Command

Berikut adalah daftar command penting Laravel Artisan yang sering digunakan dalam pengembangan project. Agar lebih mudah dipahami, command dibagi menjadi beberapa kategori.

---

### Server & Aplikasi

| Command             | Fungsi                           |
| ------------------- | -------------------------------- |
| `php artisan serve` | Menjalankan server lokal Laravel |

---

### Database & Migration

| Command                       | Fungsi                                         |
| ----------------------------- | ---------------------------------------------- |
| `php artisan migrate`         | Menjalankan migrasi database                   |
| `php artisan migrate:refresh` | Reset & jalankan ulang semua migrasi           |
| `php artisan migrate:fresh`   | Hapus semua tabel lalu migrasi ulang dari awal |
| `php artisan db:seed`         | Menjalankan seeder database                    |

---

### Generator (Make Commands)

| Command                                      | Fungsi                            |
| -------------------------------------------- | --------------------------------- |
| `php artisan make:controller NamaController` | Membuat controller baru           |
| `php artisan make:model NamaModel`           | Membuat model                     |
| `php artisan make:model NamaModel -m`        | Membuat model sekaligus migration |
| `php artisan make:migration nama_migration`  | Membuat file migration baru       |
| `php artisan make:seeder NamaSeeder`         | Membuat seeder database           |

---

### Cleaning & Cache

| Command                      | Fungsi                            |
| ---------------------------- | --------------------------------- |
| `php artisan config:clear`   | Membersihkan cache konfigurasi    |
| `php artisan cache:clear`    | Membersihkan cache aplikasi       |
| `php artisan route:clear`    | Membersihkan cache route          |
| `php artisan view:clear`     | Membersihkan cache view           |
| `php artisan optimize:clear` | Membersihkan semua cache optimize |

---

### Utility & Setup

| Command                    | Fungsi                                  |
| -------------------------- | --------------------------------------- |
| `php artisan tinker`       | Terminal interaktif Laravel             |
| `php artisan key:generate` | Generate application key                |
| `php artisan storage:link` | Membuat symbolic link storage ke public |
