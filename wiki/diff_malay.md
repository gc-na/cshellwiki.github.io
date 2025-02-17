# [Linux] Bash diff Penggunaan: Membandingkan fail teks

## Overview
Perintah `diff` digunakan untuk membandingkan dua fail teks dan menunjukkan perbezaan antara mereka. Ia sangat berguna untuk pengaturcara dan penulis dokumen yang ingin melihat perubahan yang dibuat pada fail.

## Usage
Sintaks asas untuk perintah `diff` adalah seperti berikut:

```bash
diff [options] [arguments]
```

## Common Options
- `-u`: Menunjukkan perbezaan dalam format unified, yang lebih mudah dibaca.
- `-c`: Menunjukkan perbezaan dalam format context, memberikan lebih banyak konteks di sekitar perubahan.
- `-i`: Mengabaikan perbezaan dalam huruf besar dan kecil.
- `-w`: Mengabaikan ruang kosong dalam perbandingan.
- `-q`: Menunjukkan hanya sama ada fail berbeza atau tidak, tanpa menunjukkan perbezaan terperinci.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan perintah `diff`:

1. **Membandingkan dua fail teks**:
   ```bash
   diff fail1.txt fail2.txt
   ```

2. **Menggunakan format unified**:
   ```bash
   diff -u fail1.txt fail2.txt
   ```

3. **Mengabaikan huruf besar dan kecil**:
   ```bash
   diff -i fail1.txt fail2.txt
   ```

4. **Mengabaikan ruang kosong**:
   ```bash
   diff -w fail1.txt fail2.txt
   ```

5. **Menunjukkan hanya sama ada fail berbeza**:
   ```bash
   diff -q fail1.txt fail2.txt
   ```

## Tips
- Sentiasa gunakan pilihan `-u` untuk hasil yang lebih mudah dibaca, terutama jika anda bekerja dengan perubahan kod.
- Simpan salinan fail asal sebelum membuat perubahan besar, supaya anda boleh menggunakan `diff` untuk melihat perbezaan dengan mudah.
- Gunakan `diff` bersama dengan alat lain seperti `patch` untuk mengaplikasikan perubahan secara automatik.