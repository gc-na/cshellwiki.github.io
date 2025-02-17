# [Linux] Bash rev: Membalikkan baris teks

## Overview
Perintah `rev` dalam Bash digunakan untuk membalikkan setiap baris dalam fail atau input teks. Ini berguna untuk pelbagai aplikasi, termasuk pemprosesan teks dan analisis data.

## Usage
Sintaks asas untuk menggunakan perintah `rev` adalah seperti berikut:

```
rev [options] [arguments]
```

## Common Options
- `-o, --output=FILE` : Menyimpan output ke dalam fail yang ditentukan.
- `--help` : Menunjukkan maklumat bantuan tentang perintah ini.
- `--version` : Menunjukkan versi perintah `rev`.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `rev`:

1. **Membalikkan teks dari input standard:**
   ```bash
   echo "Hello World" | rev
   ```
   Output:
   ```
   dlroW olleH
   ```

2. **Membalikkan baris dalam fail:**
   ```bash
   rev nama_fail.txt
   ```

3. **Membalikkan dan menyimpan output ke fail baru:**
   ```bash
   rev nama_fail.txt -o fail_balik.txt
   ```

4. **Menggunakan rev dengan input dari fail dan output ke terminal:**
   ```bash
   rev < nama_fail.txt
   ```

## Tips
- Pastikan untuk menggunakan `rev` dengan fail teks yang tidak terlalu besar untuk mengelakkan masalah prestasi.
- Anda boleh menggabungkan `rev` dengan perintah lain menggunakan paip (`|`) untuk pemprosesan yang lebih kompleks.
- Gunakan pilihan `-o` untuk menyimpan hasil ke dalam fail jika anda ingin menyimpan output untuk penggunaan selanjutnya.