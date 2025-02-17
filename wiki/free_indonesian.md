# [Linux] Bash free: Menampilkan informasi penggunaan memori

## Overview
Perintah `free` digunakan untuk menampilkan informasi tentang penggunaan memori dalam sistem Linux. Ini memberikan gambaran umum tentang memori fisik dan swap yang tersedia, serta memori yang sedang digunakan oleh sistem.

## Usage
Sintaks dasar dari perintah `free` adalah sebagai berikut:

```bash
free [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan perintah `free`:

- `-h`: Menampilkan ukuran memori dalam format yang lebih mudah dibaca (misalnya, dalam KB, MB, atau GB).
- `-m`: Menampilkan penggunaan memori dalam megabyte.
- `-g`: Menampilkan penggunaan memori dalam gigabyte.
- `-s <detik>`: Menampilkan informasi memori secara berkala setiap <detik> yang ditentukan.
- `-t`: Menampilkan total penggunaan memori.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `free`:

1. Menampilkan informasi memori dalam format yang lebih mudah dibaca:
   ```bash
   free -h
   ```

2. Menampilkan penggunaan memori dalam megabyte:
   ```bash
   free -m
   ```

3. Menampilkan informasi memori setiap 5 detik:
   ```bash
   free -s 5
   ```

4. Menampilkan total penggunaan memori:
   ```bash
   free -t
   ```

## Tips
- Gunakan opsi `-h` untuk mendapatkan tampilan yang lebih ramah pengguna, terutama jika Anda tidak terbiasa dengan angka besar.
- Kombinasikan `free` dengan perintah lain seperti `watch` untuk memantau penggunaan memori secara real-time:
  ```bash
  watch free -h
  ```
- Perhatikan kolom `available` pada output `free`, karena ini menunjukkan jumlah memori yang dapat digunakan oleh aplikasi baru.