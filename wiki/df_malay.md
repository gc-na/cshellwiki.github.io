# [Linux] Bash df Penggunaan: Menunjukkan ruang disk yang digunakan dan tersedia

## Overview
Perintah `df` dalam Bash digunakan untuk menunjukkan ruang disk yang digunakan dan tersedia pada sistem fail. Ia memberikan maklumat tentang sistem fail yang dipasang dan membantu pengguna memahami penggunaan ruang disk mereka.

## Usage
Sintaks asas untuk perintah `df` adalah seperti berikut:

```bash
df [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk perintah `df`:

- `-h`: Menunjukkan ruang dalam format yang mudah dibaca (contohnya, dalam MB atau GB).
- `-T`: Menunjukkan jenis sistem fail untuk setiap sistem fail yang dipasang.
- `-a`: Menunjukkan semua sistem fail, termasuk yang tidak digunakan.
- `-i`: Menunjukkan penggunaan inode, bukan ruang disk.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan perintah `df`:

1. Menunjukkan ruang disk dalam format yang mudah dibaca:
   ```bash
   df -h
   ```

2. Menunjukkan jenis sistem fail untuk setiap sistem fail:
   ```bash
   df -T
   ```

3. Menunjukkan semua sistem fail, termasuk yang tidak digunakan:
   ```bash
   df -a
   ```

4. Menunjukkan penggunaan inode:
   ```bash
   df -i
   ```

## Tips
- Gunakan pilihan `-h` untuk memudahkan pemahaman tentang penggunaan ruang disk, terutamanya jika anda bekerja dengan jumlah yang besar.
- Periksa penggunaan inode dengan `df -i` jika anda mengalami masalah dengan penciptaan fail, kerana ini mungkin disebabkan oleh kehabisan inode.
- Gabungkan pilihan untuk mendapatkan maklumat yang lebih terperinci, contohnya `df -hT` untuk melihat ruang dan jenis sistem fail secara serentak.