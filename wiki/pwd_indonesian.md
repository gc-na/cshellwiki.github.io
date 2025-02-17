# [Linux] Bash pwd Penggunaan: Menampilkan direktori kerja saat ini

## Overview
Perintah `pwd` (print working directory) digunakan untuk menampilkan jalur lengkap dari direktori kerja saat ini di terminal. Ini sangat berguna untuk mengetahui lokasi Anda dalam struktur sistem file.

## Usage
Sintaks dasar dari perintah `pwd` adalah sebagai berikut:

```bash
pwd [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan perintah `pwd`:

- `-L` : Menampilkan jalur simbolik dari direktori kerja saat ini.
- `-P` : Menampilkan jalur fisik dari direktori kerja saat ini, mengabaikan tautan simbolik.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `pwd`:

1. Menampilkan direktori kerja saat ini:
   ```bash
   pwd
   ```

2. Menampilkan jalur simbolik dari direktori kerja saat ini:
   ```bash
   pwd -L
   ```

3. Menampilkan jalur fisik dari direktori kerja saat ini:
   ```bash
   pwd -P
   ```

## Tips
- Gunakan `pwd` secara berkala untuk memastikan Anda berada di direktori yang benar sebelum menjalankan perintah lain.
- Kombinasikan `pwd` dengan perintah lain seperti `cd` untuk navigasi yang lebih efisien dalam sistem file.
- Jika Anda bekerja dengan skrip, pertimbangkan untuk menyimpan output dari `pwd` dalam variabel untuk referensi di kemudian hari.