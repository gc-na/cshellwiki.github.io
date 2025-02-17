# [Linux] Bash diff Penggunaan: Membandingkan file dan direktori

## Overview
Perintah `diff` digunakan untuk membandingkan dua file atau direktori dan menampilkan perbedaan di antara keduanya. Ini sangat berguna untuk melihat perubahan yang telah dilakukan pada file teks, seperti kode sumber atau dokumen.

## Usage
Sintaks dasar untuk perintah `diff` adalah sebagai berikut:

```
diff [options] [file1] [file2]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan perintah `diff`:

- `-u`: Menampilkan perbedaan dalam format unified, yang lebih mudah dibaca.
- `-c`: Menampilkan perbedaan dalam format context, memberikan lebih banyak konteks di sekitar perubahan.
- `-i`: Mengabaikan perbedaan dalam huruf besar/kecil.
- `-w`: Mengabaikan semua spasi putih saat membandingkan.
- `-r`: Membandingkan direktori secara rekursif.

## Common Examples

1. **Membandingkan dua file teks:**
   ```bash
   diff file1.txt file2.txt
   ```

2. **Menggunakan opsi unified untuk melihat perbedaan:**
   ```bash
   diff -u file1.txt file2.txt
   ```

3. **Membandingkan dua direktori:**
   ```bash
   diff -r dir1/ dir2/
   ```

4. **Mengabaikan spasi putih saat membandingkan:**
   ```bash
   diff -w file1.txt file2.txt
   ```

5. **Menampilkan perbedaan dalam format context:**
   ```bash
   diff -c file1.txt file2.txt
   ```

## Tips
- Selalu gunakan opsi `-u` untuk hasil yang lebih mudah dibaca, terutama saat bekerja dengan file kode.
- Jika Anda bekerja dengan banyak file, pertimbangkan untuk menggunakan `diff -r` untuk membandingkan seluruh direktori.
- Gunakan `diff` bersama dengan alat lain seperti `patch` untuk menerapkan perubahan yang telah Anda buat.