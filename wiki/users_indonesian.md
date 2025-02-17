# [Linux] Pengguna Bash: Mengelola pengguna sistem

## Overview
Perintah `users` digunakan untuk menampilkan nama pengguna yang sedang aktif di sistem. Ini memberikan informasi tentang siapa yang sedang masuk ke sistem pada waktu tertentu.

## Usage
Sintaks dasar dari perintah `users` adalah sebagai berikut:

```bash
users [options]
```

## Common Options
- `-a`: Menampilkan semua nama pengguna, termasuk yang tidak sedang aktif.
- `-d`: Menampilkan daftar pengguna yang sedang aktif dalam format yang lebih terperinci.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `users`:

1. Menampilkan nama pengguna yang sedang aktif:
   ```bash
   users
   ```

2. Menampilkan semua pengguna, termasuk yang tidak aktif:
   ```bash
   users -a
   ```

3. Menampilkan daftar pengguna dalam format terperinci:
   ```bash
   users -d
   ```

## Tips
- Gunakan perintah `who` untuk mendapatkan informasi lebih lengkap tentang sesi pengguna, termasuk waktu masuk dan terminal yang digunakan.
- Perintah `w` juga dapat memberikan informasi tambahan seperti aktivitas pengguna saat ini.
- Jika Anda hanya ingin melihat jumlah pengguna yang aktif, Anda bisa menggunakan kombinasi `users | wc -w` untuk menghitung jumlahnya.