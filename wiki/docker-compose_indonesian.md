# [Sistem Operasi] C Shell (csh) docker-compose Penggunaan: Mengelola aplikasi Docker

## Overview
Perintah `docker-compose` digunakan untuk mendefinisikan dan menjalankan aplikasi multi-container Docker. Dengan menggunakan file konfigurasi, pengguna dapat dengan mudah mengelola berbagai layanan yang saling berinteraksi dalam satu aplikasi.

## Usage
Berikut adalah sintaks dasar dari perintah `docker-compose`:

```bash
docker-compose [options] [arguments]
```

## Common Options
- `up`: Membangun, (re)start, dan menjalankan semua layanan yang didefinisikan dalam file `docker-compose.yml`.
- `down`: Menghentikan dan menghapus semua container yang dibuat oleh `up`.
- `build`: Membangun atau membangun ulang layanan.
- `logs`: Melihat log dari semua layanan yang sedang berjalan.
- `ps`: Menampilkan status dari layanan yang sedang berjalan.

## Common Examples
Berikut adalah beberapa contoh penggunaan `docker-compose`:

1. **Menjalankan aplikasi dengan `docker-compose up`:**
   ```bash
   docker-compose up
   ```

2. **Menjalankan aplikasi di background (detached mode):**
   ```bash
   docker-compose up -d
   ```

3. **Menghentikan dan menghapus container dengan `docker-compose down`:**
   ```bash
   docker-compose down
   ```

4. **Melihat log dari layanan:**
   ```bash
   docker-compose logs
   ```

5. **Membangun ulang layanan:**
   ```bash
   docker-compose build
   ```

## Tips
- Selalu periksa file `docker-compose.yml` untuk memastikan semua layanan dan dependensinya didefinisikan dengan benar.
- Gunakan opsi `-d` untuk menjalankan aplikasi di background agar terminal tetap tersedia untuk perintah lain.
- Manfaatkan perintah `docker-compose logs` untuk debugging jika ada masalah dengan layanan yang berjalan.