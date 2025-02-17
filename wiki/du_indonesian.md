# [Linux] Bash du Penggunaan: Menampilkan Ukuran Direktori dan File

## Overview
Perintah `du` (disk usage) digunakan untuk menampilkan ukuran file dan direktori di sistem file. Dengan `du`, pengguna dapat mengetahui berapa banyak ruang disk yang digunakan oleh file dan subdirektori dalam suatu direktori.

## Usage
Berikut adalah sintaks dasar dari perintah `du`:

```bash
du [options] [arguments]
```

## Common Options
- `-h`: Menampilkan ukuran dalam format yang lebih mudah dibaca (human-readable), seperti KB, MB, atau GB.
- `-s`: Menampilkan total ukuran dari direktori tanpa menampilkan ukuran subdirektori.
- `-a`: Menampilkan ukuran semua file, bukan hanya direktori.
- `-c`: Menampilkan total keseluruhan di akhir output.
- `--max-depth=N`: Menentukan kedalaman maksimum subdirektori yang akan ditampilkan.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `du`:

1. Menampilkan ukuran semua file dan direktori dalam direktori saat ini:
   ```bash
   du
   ```

2. Menampilkan ukuran dalam format yang lebih mudah dibaca:
   ```bash
   du -h
   ```

3. Menampilkan total ukuran dari direktori tertentu:
   ```bash
   du -sh /path/to/directory
   ```

4. Menampilkan ukuran semua file dan direktori dengan total keseluruhan:
   ```bash
   du -ch /path/to/directory/*
   ```

5. Menampilkan ukuran hingga kedalaman tertentu:
   ```bash
   du --max-depth=1 -h /path/to/directory
   ```

## Tips
- Gunakan opsi `-h` untuk memudahkan pembacaan ukuran, terutama saat bekerja dengan direktori besar.
- Kombinasikan `du` dengan perintah lain seperti `sort` untuk mengurutkan hasil berdasarkan ukuran.
- Untuk analisis lebih lanjut, pertimbangkan menggunakan `du` bersama dengan `grep` untuk mencari direktori atau file tertentu.