# [Linux] Bash stat Penggunaan: Menampilkan informasi status file

## Overview
Perintah `stat` digunakan untuk menampilkan informasi status dari file atau direktori di sistem Linux. Informasi yang ditampilkan mencakup ukuran file, waktu akses, waktu modifikasi, dan banyak lagi.

## Usage
Sintaks dasar dari perintah `stat` adalah sebagai berikut:

```bash
stat [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan perintah `stat`:

- `-c` : Menentukan format output yang ingin ditampilkan.
- `-f` : Menampilkan informasi sistem file dari file yang ditentukan.
- `--format` : Menentukan format output secara lebih spesifik.
- `-h` : Menampilkan ukuran file dalam format yang lebih mudah dibaca (misalnya, KB, MB).

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `stat`:

1. Menampilkan informasi dasar dari sebuah file:
   ```bash
   stat namafile.txt
   ```

2. Menampilkan informasi dengan format yang lebih ringkas:
   ```bash
   stat -c '%s bytes' namafile.txt
   ```

3. Menampilkan informasi sistem file dari sebuah direktori:
   ```bash
   stat -f /path/to/directory
   ```

4. Menampilkan ukuran file dalam format yang lebih mudah dibaca:
   ```bash
   stat -h namafile.txt
   ```

## Tips
- Gunakan opsi `-c` untuk menyesuaikan output agar lebih sesuai dengan kebutuhan Anda.
- Periksa informasi waktu akses dan modifikasi untuk memahami kapan file terakhir diubah.
- Jika Anda bekerja dengan banyak file, pertimbangkan untuk menggunakan wildcard (misalnya, `*.txt`) untuk mendapatkan informasi tentang beberapa file sekaligus.