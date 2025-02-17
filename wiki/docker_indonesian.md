# [Linux] Bash docker penggunaan: Mengelola kontainer dan gambar

## Overview
Perintah `docker` digunakan untuk mengelola kontainer dan gambar dalam lingkungan Docker. Docker memungkinkan pengguna untuk mengemas aplikasi dan semua dependensinya ke dalam kontainer yang dapat dijalankan di berbagai sistem.

## Usage
Berikut adalah sintaks dasar dari perintah docker:

```bash
docker [options] [arguments]
```

## Common Options
- `run`: Menjalankan sebuah kontainer baru.
- `ps`: Menampilkan daftar kontainer yang sedang berjalan.
- `images`: Menampilkan daftar gambar yang tersedia di sistem.
- `pull`: Mengunduh gambar dari Docker Hub.
- `build`: Membangun gambar dari Dockerfile.
- `exec`: Menjalankan perintah di dalam kontainer yang sedang berjalan.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah docker:

1. **Menjalankan kontainer baru:**
   ```bash
   docker run -d -p 80:80 nginx
   ```
   Perintah ini menjalankan kontainer Nginx di latar belakang dan memetakan port 80 kontainer ke port 80 host.

2. **Menampilkan kontainer yang sedang berjalan:**
   ```bash
   docker ps
   ```
   Perintah ini menampilkan daftar kontainer yang saat ini aktif.

3. **Mengunduh gambar dari Docker Hub:**
   ```bash
   docker pull ubuntu
   ```
   Perintah ini mengunduh gambar Ubuntu terbaru dari Docker Hub.

4. **Membangun gambar dari Dockerfile:**
   ```bash
   docker build -t myapp .
   ```
   Perintah ini membangun gambar dengan nama `myapp` dari Dockerfile yang ada di direktori saat ini.

5. **Menjalankan perintah di dalam kontainer:**
   ```bash
   docker exec -it my_container bash
   ```
   Perintah ini membuka shell bash di dalam kontainer yang bernama `my_container`.

## Tips
- Selalu gunakan tag versi saat menarik gambar untuk menghindari perubahan yang tidak terduga.
- Gunakan `docker-compose` untuk mengelola beberapa kontainer dengan lebih mudah.
- Pastikan untuk membersihkan kontainer dan gambar yang tidak terpakai dengan perintah `docker system prune` untuk menghemat ruang disk.