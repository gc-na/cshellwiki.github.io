# [Linux] Bash docker-compose Penggunaan: Mengelola aplikasi Docker

## Overview
Perintah `docker-compose` digunakan untuk mendefinisikan dan menjalankan aplikasi multi-kontainer Docker. Dengan menggunakan file konfigurasi YAML, pengguna dapat mengatur layanan, jaringan, dan volume yang diperlukan untuk aplikasi mereka dengan mudah.

## Usage
Berikut adalah sintaks dasar dari perintah `docker-compose`:

```bash
docker-compose [options] [arguments]
```

## Common Options
- `up`: Menjalankan kontainer yang ditentukan dalam file `docker-compose.yml`.
- `down`: Menghentikan dan menghapus kontainer yang sedang berjalan.
- `build`: Membangun atau membangun ulang layanan.
- `logs`: Melihat log dari kontainer yang sedang berjalan.
- `ps`: Menampilkan daftar kontainer yang dikelola oleh docker-compose.

## Common Examples
Berikut adalah beberapa contoh penggunaan `docker-compose`:

1. **Menjalankan aplikasi**:
   ```bash
   docker-compose up
   ```

2. **Menjalankan aplikasi di background**:
   ```bash
   docker-compose up -d
   ```

3. **Menghentikan dan menghapus kontainer**:
   ```bash
   docker-compose down
   ```

4. **Melihat log dari kontainer**:
   ```bash
   docker-compose logs
   ```

5. **Membangun ulang layanan**:
   ```bash
   docker-compose build
   ```

## Tips
- Selalu gunakan file `docker-compose.yml` untuk mendefinisikan semua layanan dan konfigurasi yang diperlukan agar lebih terorganisir.
- Gunakan opsi `-d` untuk menjalankan kontainer di latar belakang, sehingga terminal Anda tetap bebas untuk digunakan.
- Periksa log secara berkala untuk memastikan bahwa semua layanan berjalan dengan baik dan untuk mengidentifikasi masalah lebih awal.