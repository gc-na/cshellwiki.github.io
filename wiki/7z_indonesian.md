# [Linux] Bash 7z Penggunaan: Mengompres dan mengekstrak file

## Overview
Perintah `7z` adalah alat baris perintah yang digunakan untuk mengompres dan mengekstrak file menggunakan format arsip 7z. Ini adalah bagian dari perangkat lunak 7-Zip yang terkenal karena rasio kompresi yang tinggi dan dukungan untuk berbagai format arsip.

## Usage
Sintaks dasar dari perintah `7z` adalah sebagai berikut:

```
7z [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan perintah `7z`:

- `a`: Menambahkan file ke arsip.
- `x`: Mengekstrak file dari arsip.
- `l`: Menampilkan daftar file dalam arsip.
- `d`: Menghapus file dari arsip.
- `t`: Menguji integritas arsip.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `7z`:

1. **Mengompres file atau direktori:**
   ```bash
   7z a arsip.7z file1.txt file2.txt
   ```

2. **Mengekstrak file dari arsip:**
   ```bash
   7z x arsip.7z
   ```

3. **Menampilkan daftar isi arsip:**
   ```bash
   7z l arsip.7z
   ```

4. **Menghapus file dari arsip:**
   ```bash
   7z d arsip.7z file1.txt
   ```

5. **Menguji integritas arsip:**
   ```bash
   7z t arsip.7z
   ```

## Tips
- Selalu periksa ukuran file setelah kompresi untuk memastikan efisiensi kompresi.
- Gunakan opsi `-p` untuk menambahkan kata sandi pada arsip yang ingin Anda lindungi.
- Untuk kompresi yang lebih baik, pertimbangkan untuk menggunakan opsi `-mx=9` yang mengatur tingkat kompresi maksimum.