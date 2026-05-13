# Setup PHP dan Laravel

Cek Versi:

```sh
    php -v
    composer -V
```

## 1. Buat Project Laravel

```sh
composer create-project laravel/laravel myapp
```

## 2. Masuk ke Folder Project

```sh
cd myapp
```

## 3. Jalankan Laravel

```sh
php artisan serve
```

Buka browser:

```sh
http://127.0.0.1:8000
```

## 4. Setup Database

Buka file:

```sh
.env
```

Ubah:

```sh
DB_DATABASE=laravel_db
DB_USERNAME=root
DB_PASSWORD=
```

Pastikan database sudah dibuat di `phpMyAdmin`

## 6. Struktur yang wajib

```sh
routes/web.php          → URL
app/Http/Controllers/   → logic
resources/views/        → tampilan
.env                    → config
```
