# [Linux] Bash nl Penggunaan: Menampilkan nomor baris dalam file teks

## Overview
Perintah `nl` digunakan untuk menampilkan isi file teks dengan menambahkan nomor baris di sebelah kiri setiap baris. Ini sangat berguna untuk memudahkan referensi dan navigasi dalam file yang panjang.

## Usage
Berikut adalah sintaks dasar dari perintah `nl`:

```bash
nl [options] [arguments]
```

## Common Options
- `-b` : Menentukan cara penomoran baris (misalnya, `-b a` untuk menomori semua baris).
- `-f` : Menentukan baris yang tidak akan dinomori (misalnya, `-f 2` untuk tidak menomori baris kedua).
- `-h` : Menentukan header yang akan ditampilkan di atas nomor baris.
- `-n` : Menentukan format penomoran (misalnya, `-n ln` untuk nomor baris dengan nol di depan).

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `nl`:

1. Menampilkan nomor baris dari file `contoh.txt`:
   ```bash
   nl contoh.txt
   ```

2. Menampilkan nomor baris dengan format nol di depan:
   ```bash
   nl -n ln contoh.txt
   ```

3. Menampilkan nomor baris tetapi melewatkan baris kosong:
   ```bash
   nl -b a contoh.txt
   ```

4. Menggunakan header untuk menampilkan judul sebelum nomor baris:
   ```bash
   nl -h "Isi File" contoh.txt
   ```

## Tips
- Gunakan opsi `-b` untuk mengontrol baris mana yang dinomori, sehingga Anda dapat menyesuaikan output sesuai kebutuhan.
- Cobalah menggabungkan `nl` dengan perintah lain seperti `grep` untuk menomori hasil pencarian dalam file.
- Pastikan untuk memeriksa file yang sangat besar, karena output `nl` bisa menjadi panjang dan sulit dibaca tanpa pengaturan yang tepat.