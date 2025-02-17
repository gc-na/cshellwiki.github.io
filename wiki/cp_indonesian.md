# [Linux] Bash cp Penggunaan: Menyalin file dan direktori

## Overview
Perintah `cp` digunakan untuk menyalin file dan direktori di sistem operasi berbasis Unix, seperti Linux. Dengan `cp`, Anda dapat membuat salinan file atau seluruh direktori dengan mudah.

## Usage
Berikut adalah sintaks dasar dari perintah `cp`:

```bash
cp [options] [source] [destination]
```

## Common Options
Berikut adalah beberapa opsi umum yang digunakan dengan perintah `cp`:

- `-r` : Menyalin direktori secara rekursif.
- `-i` : Meminta konfirmasi sebelum menimpa file yang ada.
- `-u` : Menyalin hanya jika sumber lebih baru daripada tujuan atau jika tujuan tidak ada.
- `-v` : Menampilkan nama file yang sedang disalin.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `cp`:

1. Menyalin file dari satu lokasi ke lokasi lain:
   ```bash
   cp file1.txt /home/user/directory/
   ```

2. Menyalin file dan menimpa file yang ada tanpa konfirmasi:
   ```bash
   cp -f file1.txt file2.txt
   ```

3. Menyalin direktori beserta isinya:
   ```bash
   cp -r /home/user/source_directory /home/user/destination_directory
   ```

4. Menyalin file dan menampilkan prosesnya:
   ```bash
   cp -v file1.txt /home/user/directory/
   ```

5. Menyalin file hanya jika file sumber lebih baru:
   ```bash
   cp -u file1.txt /home/user/directory/
   ```

## Tips
- Selalu gunakan opsi `-i` jika Anda tidak ingin menimpa file yang ada tanpa konfirmasi.
- Gunakan opsi `-v` untuk melihat proses penyalinan, terutama saat menyalin banyak file.
- Jika menyalin direktori, pastikan untuk selalu menggunakan opsi `-r` agar semua isi direktori juga disalin.