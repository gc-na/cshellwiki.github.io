# [Linux] Bash sort penggunaan: Mengurutkan baris teks

## Overview
Perintah `sort` dalam Bash digunakan untuk mengurutkan baris teks dalam file atau dari input standar. Perintah ini sangat berguna untuk mengorganisir data, membuatnya lebih mudah dibaca dan dianalisis.

## Usage
Berikut adalah sintaks dasar dari perintah `sort`:

```bash
sort [options] [arguments]
```

## Common Options
- `-r`: Mengurutkan dalam urutan terbalik (descending).
- `-n`: Mengurutkan berdasarkan nilai numerik.
- `-k`: Mengurutkan berdasarkan kolom tertentu.
- `-u`: Menghapus duplikat dari hasil yang diurutkan.
- `-o`: Menyimpan hasil ke dalam file yang ditentukan.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `sort`:

1. Mengurutkan isi file secara alfabetis:
   ```bash
   sort namafile.txt
   ```

2. Mengurutkan isi file dalam urutan terbalik:
   ```bash
   sort -r namafile.txt
   ```

3. Mengurutkan angka dalam file:
   ```bash
   sort -n angka.txt
   ```

4. Mengurutkan berdasarkan kolom tertentu (misalnya kolom kedua):
   ```bash
   sort -k2 namafile.txt
   ```

5. Menghapus duplikat dan menyimpan hasil ke file baru:
   ```bash
   sort -u namafile.txt -o hasil.txt
   ```

## Tips
- Gunakan opsi `-o` untuk menyimpan hasil pengurutan langsung ke file, sehingga Anda tidak perlu mengalihkan output ke terminal.
- Kombinasikan opsi untuk hasil yang lebih spesifik, seperti `sort -n -r` untuk mengurutkan angka dalam urutan terbalik.
- Periksa file yang berisi data terpisah dengan koma atau spasi, dan gunakan opsi `-t` untuk menentukan pemisah jika diperlukan.