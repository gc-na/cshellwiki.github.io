# [Linux] Bash df Penggunaan: Menampilkan informasi penggunaan disk

## Overview
Perintah `df` digunakan untuk menampilkan informasi tentang penggunaan ruang disk pada sistem file. Ini memberikan gambaran tentang seberapa banyak ruang yang digunakan dan tersedia pada setiap sistem file yang terpasang.

## Usage
Sintaks dasar dari perintah `df` adalah sebagai berikut:

```bash
df [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan perintah `df`:

- `-h`: Menampilkan ukuran dalam format yang lebih mudah dibaca (misalnya, KB, MB, GB).
- `-T`: Menampilkan tipe sistem file.
- `-a`: Menampilkan semua sistem file, termasuk yang tidak terpakai.
- `-i`: Menampilkan informasi tentang inode, bukan penggunaan ruang disk.

## Common Examples
Berikut adalah beberapa contoh praktis penggunaan perintah `df`:

1. Menampilkan informasi penggunaan disk dalam format yang mudah dibaca:
   ```bash
   df -h
   ```

2. Menampilkan informasi penggunaan disk beserta tipe sistem file:
   ```bash
   df -hT
   ```

3. Menampilkan semua sistem file, termasuk yang tidak terpakai:
   ```bash
   df -a
   ```

4. Menampilkan informasi tentang inode:
   ```bash
   df -i
   ```

## Tips
- Gunakan opsi `-h` untuk memudahkan pemahaman informasi yang ditampilkan, terutama jika Anda bekerja dengan sistem file besar.
- Periksa penggunaan inode dengan `df -i` jika Anda mengalami masalah dengan pembuatan file baru, karena kehabisan inode dapat terjadi meskipun ruang disk masih tersedia.
- Untuk pemantauan berkala, pertimbangkan untuk menggabungkan `df` dengan perintah lain seperti `watch` untuk melihat perubahan penggunaan disk secara real-time:
  ```bash
  watch df -h
  ```