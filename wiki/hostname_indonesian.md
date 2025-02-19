# [Sistem Operasi] C Shell (csh) hostname: Menampilkan atau mengatur nama host

## Overview
Perintah `hostname` digunakan untuk menampilkan atau mengatur nama host dari sistem yang sedang digunakan. Nama host adalah identifikasi unik untuk perangkat dalam jaringan, yang memungkinkan perangkat lain untuk mengenalinya.

## Usage
Berikut adalah sintaks dasar dari perintah `hostname`:

```
hostname [options] [arguments]
```

## Common Options
- `-f`: Menampilkan nama host lengkap (fully qualified domain name).
- `-s`: Menampilkan hanya nama host singkat.
- `-i`: Menampilkan alamat IP dari nama host.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `hostname`:

1. Menampilkan nama host saat ini:
   ```csh
   hostname
   ```

2. Menampilkan nama host lengkap:
   ```csh
   hostname -f
   ```

3. Menampilkan nama host singkat:
   ```csh
   hostname -s
   ```

4. Mengatur nama host baru:
   ```csh
   hostname new-hostname
   ```

5. Menampilkan alamat IP dari nama host:
   ```csh
   hostname -i
   ```

## Tips
- Pastikan Anda memiliki hak akses yang diperlukan untuk mengubah nama host.
- Setelah mengubah nama host, Anda mungkin perlu me-reboot sistem agar perubahan dapat diterapkan sepenuhnya.
- Gunakan opsi `-f` untuk mendapatkan informasi lengkap tentang nama host, terutama jika Anda bekerja dalam lingkungan jaringan yang kompleks.