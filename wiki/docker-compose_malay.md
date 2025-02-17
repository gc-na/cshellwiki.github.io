# [Linux] Bash docker-compose Penggunaan: Mengurus aplikasi berbilang kontena

## Overview
Perintah `docker-compose` digunakan untuk mengurus aplikasi yang terdiri daripada beberapa kontena Docker. Ia membolehkan pengguna untuk mendefinisikan dan menjalankan aplikasi dalam satu fail konfigurasi, menjadikan pengurusan kontena lebih mudah dan teratur.

## Usage
Berikut adalah sintaks asas untuk menggunakan `docker-compose`:

```bash
docker-compose [options] [arguments]
```

## Common Options
- `up`: Membangunkan dan menjalankan semua kontena yang ditakrifkan dalam fail `docker-compose.yml`.
- `down`: Menghentikan dan menghapuskan semua kontena yang sedang berjalan.
- `build`: Membangunkan imej kontena berdasarkan konfigurasi dalam fail `docker-compose.yml`.
- `logs`: Memaparkan log untuk semua kontena yang sedang berjalan.
- `exec`: Menjalankan arahan dalam kontena yang sedang berjalan.

## Common Examples
Berikut adalah beberapa contoh penggunaan `docker-compose`:

1. **Membangunkan aplikasi:**
   ```bash
   docker-compose up
   ```

2. **Menghentikan dan menghapuskan kontena:**
   ```bash
   docker-compose down
   ```

3. **Membangunkan imej kontena:**
   ```bash
   docker-compose build
   ```

4. **Melihat log kontena:**
   ```bash
   docker-compose logs
   ```

5. **Menjalankan arahan dalam kontena:**
   ```bash
   docker-compose exec <service_name> <command>
   ```

## Tips
- Sentiasa gunakan fail `docker-compose.yml` untuk mendefinisikan konfigurasi aplikasi anda dengan jelas.
- Gunakan `docker-compose up -d` untuk menjalankan kontena di latar belakang.
- Periksa kesihatan kontena dengan `docker-compose ps` untuk memastikan semuanya berjalan dengan baik.
- Simpan versi fail `docker-compose.yml` anda untuk memudahkan pengurusan dan pemulihan.