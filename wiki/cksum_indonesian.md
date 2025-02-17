# [Linux] Bash cksum Penggunaan: Menghitung checksum file

## Overview
Perintah `cksum` digunakan untuk menghitung checksum dari file. Checksum adalah nilai numerik yang dihasilkan dari konten file, yang dapat digunakan untuk memverifikasi integritas data. Dengan menggunakan `cksum`, Anda dapat memastikan bahwa file tidak telah diubah atau rusak.

## Usage
Sintaks dasar dari perintah `cksum` adalah sebagai berikut:
```
cksum [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang tersedia untuk `cksum`:
- `-a, --algorithm=ALGORITHM` : Menentukan algoritma checksum yang akan digunakan.
- `-h, --help` : Menampilkan bantuan tentang penggunaan perintah.
- `-V, --version` : Menampilkan versi dari perintah `cksum`.

## Common Examples
Berikut adalah beberapa contoh penggunaan `cksum`:

1. Menghitung checksum dari sebuah file:
   ```bash
   cksum file.txt
   ```

2. Menghitung checksum dari beberapa file sekaligus:
   ```bash
   cksum file1.txt file2.txt
   ```

3. Menggunakan opsi untuk menampilkan versi:
   ```bash
   cksum --version
   ```

4. Menggunakan opsi bantuan untuk melihat informasi lebih lanjut:
   ```bash
   cksum --help
   ```

## Tips
- Selalu periksa checksum file setelah mengunduh untuk memastikan file tidak rusak.
- Simpan nilai checksum yang dihasilkan untuk referensi di masa mendatang.
- Gunakan `cksum` bersama dengan perintah lain seperti `find` untuk memeriksa banyak file dalam satu perintah.