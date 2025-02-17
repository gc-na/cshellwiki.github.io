# [Linux] Bash hostname Penggunaan: Menampilkan atau mengatur nama host

## Overview
Perintah `hostname` digunakan untuk menampilkan atau mengatur nama host dari sistem. Nama host adalah label yang digunakan untuk mengidentifikasi perangkat dalam jaringan. Dengan menggunakan perintah ini, pengguna dapat dengan mudah mengetahui nama host saat ini atau mengubahnya sesuai kebutuhan.

## Usage
Berikut adalah sintaks dasar dari perintah `hostname`:

```bash
hostname [options] [arguments]
```

## Common Options
- `-f` : Menampilkan nama host penuh (fully qualified domain name).
- `-i` : Menampilkan alamat IP dari nama host.
- `-s` : Menampilkan nama host singkat.
- `-A` : Menampilkan semua nama alias dari host.
- `--help` : Menampilkan informasi bantuan tentang penggunaan perintah.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `hostname`:

1. Menampilkan nama host saat ini:
   ```bash
   hostname
   ```

2. Menampilkan nama host penuh:
   ```bash
   hostname -f
   ```

3. Menampilkan alamat IP dari nama host:
   ```bash
   hostname -i
   ```

4. Mengubah nama host:
   ```bash
   sudo hostname new-hostname
   ```

5. Menampilkan semua nama alias dari host:
   ```bash
   hostname -A
   ```

## Tips
- Pastikan untuk menggunakan `sudo` saat mengubah nama host agar memiliki izin yang cukup.
- Setelah mengubah nama host, pertimbangkan untuk me-reboot sistem agar perubahan diterapkan dengan benar.
- Gunakan `hostname -s` untuk mendapatkan nama host singkat yang berguna dalam skrip atau konfigurasi jaringan.