# [Linux] Bash comm penggunaan: Membandingkan dua fail baris

## Overview
Perintah `comm` digunakan untuk membandingkan dua fail teks yang disusun dan menghasilkan output yang menunjukkan baris yang unik kepada setiap fail serta baris yang sama di antara kedua-duanya. Ini berguna untuk melihat perbezaan dan persamaan antara dua set data.

## Usage
Sintaks asas untuk perintah `comm` adalah seperti berikut:

```bash
comm [options] [file1] [file2]
```

## Common Options
- `-1`: Jangan outputkan baris yang hanya terdapat dalam fail pertama.
- `-2`: Jangan outputkan baris yang hanya terdapat dalam fail kedua.
- `-3`: Jangan outputkan baris yang terdapat dalam kedua-dua fail.
- `-i`: Abaikan kes dalam perbandingan.
- `-d`: Outputkan baris yang sama tetapi hanya sekali.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `comm`:

1. **Membandingkan dua fail:**
   ```bash
   comm file1.txt file2.txt
   ```

2. **Hanya menunjukkan baris yang terdapat dalam fail pertama:**
   ```bash
   comm -13 file1.txt file2.txt
   ```

3. **Hanya menunjukkan baris yang terdapat dalam fail kedua:**
   ```bash
   comm -12 file1.txt file2.txt
   ```

4. **Mengabaikan kes dalam perbandingan:**
   ```bash
   comm -i file1.txt file2.txt
   ```

5. **Menunjukkan hanya baris yang sama:**
   ```bash
   comm -d file1.txt file2.txt
   ```

## Tips
- Pastikan fail yang ingin dibandingkan disusun secara alfabet sebelum menggunakan `comm`, kerana perintah ini berfungsi dengan baik hanya pada fail yang telah disusun.
- Gunakan pilihan `-i` jika anda ingin mengabaikan perbezaan kes, terutamanya berguna dalam fail yang mengandungi nama atau istilah yang mungkin ditulis dengan cara yang berbeza.
- Untuk analisis yang lebih mendalam, pertimbangkan untuk menggabungkan `comm` dengan perintah lain seperti `sort` untuk memastikan fail disusun dengan betul sebelum perbandingan.