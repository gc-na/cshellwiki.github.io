# [Linux] Bash sort penggunaan: Mengatur baris dalam fail teks

## Overview
Perintah `sort` digunakan untuk mengatur baris dalam fail teks. Ia menyusun baris berdasarkan urutan abjad atau numerik, menjadikannya berguna untuk menganalisis dan memproses data.

## Usage
Sintaks asas untuk perintah `sort` adalah seperti berikut:

```bash
sort [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan umum untuk perintah `sort`:

- `-n`: Mengatur secara numerik.
- `-r`: Mengatur dalam urutan terbalik.
- `-k`: Mengatur berdasarkan kolom tertentu.
- `-u`: Menghapus baris yang duplikat.
- `-o`: Menyimpan hasil ke dalam fail.

## Common Examples
Berikut adalah beberapa contoh praktikal menggunakan perintah `sort`:

1. **Mengatur fail teks secara abjad:**
   ```bash
   sort nama_fail.txt
   ```

2. **Mengatur fail teks secara numerik:**
   ```bash
   sort -n nombor_fail.txt
   ```

3. **Mengatur fail dan menyimpan hasil ke dalam fail baru:**
   ```bash
   sort nama_fail.txt -o fail_teratur.txt
   ```

4. **Menghapus baris yang duplikat:**
   ```bash
   sort -u nama_fail.txt
   ```

5. **Mengatur berdasarkan kolom kedua:**
   ```bash
   sort -k2 nama_fail.txt
   ```

## Tips
- Sentiasa gunakan pilihan `-o` untuk menyimpan hasil ke dalam fail baru jika anda ingin mengelakkan kehilangan data asal.
- Untuk fail besar, pertimbangkan untuk menggunakan `sort` dengan pilihan `-S` untuk menetapkan saiz memori yang digunakan.
- Gunakan pilihan `-r` untuk mendapatkan urutan terbalik jika diperlukan, seperti untuk mendapatkan nilai tertinggi terlebih dahulu.