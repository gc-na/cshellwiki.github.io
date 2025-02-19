# [Sistem Operasi] C Shell (csh) head: Menampilkan beberapa baris teratas dari file

## Overview
Perintah `head` digunakan untuk menampilkan beberapa baris teratas dari file teks. Secara default, `head` akan menampilkan 10 baris pertama, tetapi pengguna dapat mengubah jumlah baris yang ditampilkan sesuai kebutuhan.

## Usage
Berikut adalah sintaks dasar dari perintah `head`:

```
head [options] [arguments]
```

## Common Options
- `-n [jumlah]`: Menentukan jumlah baris yang ingin ditampilkan. Misalnya, `-n 5` untuk menampilkan 5 baris pertama.
- `-q`: Tidak menampilkan nama file saat menampilkan output dari beberapa file.
- `-v`: Menampilkan nama file sebelum output, bahkan jika hanya satu file yang diproses.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `head`:

1. Menampilkan 10 baris pertama dari file `data.txt`:
   ```csh
   head data.txt
   ```

2. Menampilkan 5 baris pertama dari file `data.txt`:
   ```csh
   head -n 5 data.txt
   ```

3. Menampilkan 3 baris pertama dari beberapa file sekaligus:
   ```csh
   head -n 3 file1.txt file2.txt
   ```

4. Menampilkan 10 baris pertama dari output perintah lain, misalnya `ls`:
   ```csh
   ls -l | head
   ```

## Tips
- Gunakan opsi `-n` untuk menyesuaikan jumlah baris yang ingin ditampilkan sesuai kebutuhan.
- Kombinasikan `head` dengan perintah lain menggunakan pipe (`|`) untuk memfilter output.
- Jika Anda bekerja dengan banyak file, pertimbangkan untuk menggunakan opsi `-q` untuk menghindari kebingungan dengan nama file yang ditampilkan.