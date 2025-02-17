# [Linux] Bash fg Penggunaan: Mengembalikan proses ke latar depan

## Overview
Perintah `fg` dalam Bash digunakan untuk mengembalikan proses yang sedang berjalan di latar belakang ke latar depan. Ini sangat berguna ketika Anda ingin berinteraksi dengan proses yang sebelumnya Anda jalankan di latar belakang.

## Usage
Berikut adalah sintaks dasar dari perintah `fg`:

```
fg [options] [job_spec]
```

## Common Options
- `job_spec`: Menentukan proses yang ingin Anda kembalikan ke latar depan. Anda dapat menggunakan nomor pekerjaan (job number) atau nama proses.
- `+`: Mengembalikan proses terakhir yang dijalankan di latar belakang.
- `-`: Mengembalikan proses kedua terakhir yang dijalankan di latar belakang.

## Common Examples

1. Mengembalikan proses terakhir yang berjalan di latar belakang:
   ```bash
   fg
   ```

2. Mengembalikan proses tertentu dengan nomor pekerjaan, misalnya pekerjaan nomor 1:
   ```bash
   fg %1
   ```

3. Mengembalikan proses kedua terakhir yang berjalan di latar belakang:
   ```bash
   fg -
   ```

4. Mengembalikan proses dengan nama tertentu (jika ada):
   ```bash
   fg %nama_proses
   ```

## Tips
- Pastikan untuk memeriksa daftar proses latar belakang Anda dengan menggunakan perintah `jobs` sebelum menggunakan `fg`.
- Jika Anda sering beralih antara proses latar depan dan latar belakang, pertimbangkan untuk menggunakan `Ctrl+Z` untuk menghentikan proses dan mengirimnya ke latar belakang sebelum menggunakan `fg`.
- Gunakan `bg` jika Anda ingin melanjutkan proses di latar belakang tanpa mengembalikannya ke latar depan.