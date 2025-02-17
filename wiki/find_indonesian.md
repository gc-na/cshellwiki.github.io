# [Linux] Bash find Penggunaan: Mencari nama file

## Overview
Perintah `find` digunakan untuk mencari file dan direktori dalam sistem file berdasarkan kriteria tertentu. Dengan `find`, pengguna dapat menemukan file berdasarkan nama, ukuran, waktu modifikasi, dan banyak lagi.

## Usage
Berikut adalah sintaks dasar dari perintah `find`:

```
find [options] [arguments]
```

## Common Options
- `-name`: Mencari file berdasarkan nama.
- `-type`: Menentukan tipe file yang dicari (misalnya, `f` untuk file biasa, `d` untuk direktori).
- `-size`: Mencari file berdasarkan ukuran.
- `-mtime`: Mencari file yang dimodifikasi dalam jangka waktu tertentu.
- `-exec`: Menjalankan perintah pada file yang ditemukan.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `find`:

1. Mencari file dengan nama tertentu:
   ```bash
   find /path/to/search -name "file.txt"
   ```

2. Mencari semua direktori dalam direktori tertentu:
   ```bash
   find /path/to/search -type d
   ```

3. Mencari file yang lebih besar dari 1MB:
   ```bash
   find /path/to/search -size +1M
   ```

4. Mencari file yang dimodifikasi dalam 7 hari terakhir:
   ```bash
   find /path/to/search -mtime -7
   ```

5. Menjalankan perintah `ls` pada setiap file yang ditemukan:
   ```bash
   find /path/to/search -name "*.txt" -exec ls -l {} \;
   ```

## Tips
- Gunakan opsi `-iname` jika Anda ingin pencarian tidak case-sensitive.
- Kombinasikan beberapa opsi untuk mempersempit hasil pencarian.
- Selalu gunakan path absolut untuk menghindari kebingungan dengan direktori saat ini.
- Pertimbangkan untuk menggunakan `-print` untuk menampilkan hasil pencarian jika Anda tidak menggunakan `-exec`.