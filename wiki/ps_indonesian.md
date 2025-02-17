# [Linux] Bash ps Penggunaan: Menampilkan proses yang sedang berjalan

## Overview
Perintah `ps` digunakan untuk menampilkan informasi tentang proses yang sedang berjalan di sistem. Ini memberikan gambaran tentang proses yang aktif, termasuk ID proses, penggunaan CPU, dan status proses.

## Usage
Sintaks dasar dari perintah `ps` adalah sebagai berikut:

```bash
ps [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang digunakan dengan perintah `ps`:

- `-e` atau `-A`: Menampilkan semua proses yang sedang berjalan.
- `-f`: Menampilkan informasi proses dalam format yang lebih lengkap.
- `-u [user]`: Menampilkan proses yang dimiliki oleh pengguna tertentu.
- `-aux`: Menampilkan semua proses dengan informasi yang lebih detail.
- `--sort`: Mengurutkan output berdasarkan kolom tertentu, seperti penggunaan CPU atau memori.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `ps`:

1. Menampilkan semua proses yang sedang berjalan:
   ```bash
   ps -e
   ```

2. Menampilkan proses dengan format yang lebih lengkap:
   ```bash
   ps -f
   ```

3. Menampilkan proses yang dimiliki oleh pengguna tertentu:
   ```bash
   ps -u username
   ```

4. Menampilkan semua proses dengan informasi detail:
   ```bash
   ps aux
   ```

5. Mengurutkan proses berdasarkan penggunaan CPU:
   ```bash
   ps aux --sort=-%cpu
   ```

## Tips
- Gunakan `ps aux` untuk mendapatkan gambaran lengkap tentang semua proses yang berjalan, termasuk yang tidak dimiliki oleh pengguna saat ini.
- Kombinasikan `ps` dengan perintah lain seperti `grep` untuk mencari proses tertentu. Contoh:
  ```bash
  ps aux | grep firefox
  ```
- Jika Anda ingin memantau proses secara real-time, pertimbangkan untuk menggunakan perintah `top` atau `htop` sebagai alternatif.