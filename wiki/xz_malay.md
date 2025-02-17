# [Linux] Bash xz Penggunaan: Memampatkan dan menyahmampatkan fail

## Overview
Perintah `xz` digunakan untuk memampatkan dan menyahmampatkan fail menggunakan algoritma pemampatan LZMA. Ia sangat berkesan dalam mengurangkan saiz fail, menjadikannya berguna untuk penyimpanan dan pemindahan data.

## Usage
Sintaks asas untuk menggunakan perintah `xz` adalah seperti berikut:

```bash
xz [options] [arguments]
```

## Common Options
- `-d`, `--decompress`: Menyahmampat fail.
- `-k`, `--keep`: Menyimpan fail asal selepas pemampatan.
- `-v`, `--verbose`: Menunjukkan maklumat lanjut semasa pemampatan.
- `-9`: Menggunakan tahap pemampatan maksimum (lebih perlahan tetapi saiz fail lebih kecil).
- `-z`: Memampatkan fail (ini adalah pilihan lalai).

## Common Examples
1. **Memampatkan fail:**
   ```bash
   xz fail.txt
   ```
   Ini akan menghasilkan fail `fail.txt.xz` dan menghapuskan `fail.txt`.

2. **Menyahmampatkan fail:**
   ```bash
   xz -d fail.txt.xz
   ```
   Ini akan mengembalikan fail asal `fail.txt` dan menghapuskan `fail.txt.xz`.

3. **Menyimpan fail asal semasa memampatkan:**
   ```bash
   xz -k fail.txt
   ```
   Ini akan menghasilkan `fail.txt.xz` tetapi mengekalkan `fail.txt`.

4. **Memampatkan dengan tahap maksimum:**
   ```bash
   xz -9 fail.txt
   ```
   Ini akan memampatkan `fail.txt` dengan tahap pemampatan tertinggi.

## Tips
- Gunakan pilihan `-v` untuk melihat proses pemampatan dan maklumat saiz fail.
- Jika anda sering bekerja dengan fail besar, pertimbangkan untuk menggunakan pilihan `-k` untuk mengelakkan kehilangan fail asal.
- Untuk pemampatan yang lebih cepat, gunakan tahap pemampatan yang lebih rendah seperti `-1` atau `-2`.