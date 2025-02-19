# [Sistem Operasi] C Shell (csh) df Penggunaan: Menampilkan informasi penggunaan disk

## Overview
Perintah `df` digunakan untuk menampilkan informasi tentang penggunaan ruang disk pada sistem file. Ini memberikan gambaran umum tentang berapa banyak ruang yang digunakan dan tersedia di setiap sistem file yang terpasang.

## Usage
Sintaks dasar dari perintah `df` adalah sebagai berikut:

```
df [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan perintah `df`:

- `-h`: Menampilkan ukuran dalam format yang lebih mudah dibaca (misalnya, KB, MB, GB).
- `-T`: Menampilkan tipe sistem file untuk setiap sistem file yang terdaftar.
- `-i`: Menampilkan informasi tentang inode, bukan penggunaan ruang disk.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `df`:

1. Menampilkan penggunaan disk dasar:
   ```bash
   df
   ```

2. Menampilkan penggunaan disk dengan ukuran yang lebih mudah dibaca:
   ```bash
   df -h
   ```

3. Menampilkan tipe sistem file:
   ```bash
   df -T
   ```

4. Menampilkan informasi inode:
   ```bash
   df -i
   ```

## Tips
- Gunakan opsi `-h` untuk memudahkan pemahaman saat melihat penggunaan disk, terutama pada sistem dengan banyak data.
- Periksa penggunaan disk secara berkala untuk menghindari kehabisan ruang yang dapat mengganggu kinerja sistem.
- Kombinasikan `df` dengan perintah lain seperti `grep` untuk memfilter hasil berdasarkan sistem file tertentu.