# [Linux] Bash iconv Penggunaan: Penukaran antara set karakter

## Overview
Perintah `iconv` digunakan untuk menukar set karakter dari satu format ke format yang lain. Ini berguna ketika anda perlu mengubah encoding fail teks untuk memastikan keserasian dengan aplikasi lain atau sistem yang berbeza.

## Usage
Berikut adalah sintaks asas untuk perintah `iconv`:

```bash
iconv [options] [arguments]
```

## Common Options
- `-f, --from-code=CODE` : Menentukan set karakter asal.
- `-t, --to-code=CODE` : Menentukan set karakter sasaran.
- `-o, --output=FILE` : Menyimpan output ke dalam fail yang ditentukan.
- `-c` : Mengabaikan karakter yang tidak boleh ditukarkan.
- `-s` : Menyembunyikan amaran tentang karakter yang tidak boleh ditukarkan.

## Common Examples
1. Menukar fail teks dari UTF-8 ke ISO-8859-1:
   ```bash
   iconv -f UTF-8 -t ISO-8859-1 input.txt -o output.txt
   ```

2. Menukar fail teks dari Windows-1252 ke UTF-8:
   ```bash
   iconv -f WINDOWS-1252 -t UTF-8 input.txt -o output.txt
   ```

3. Mengabaikan karakter yang tidak boleh ditukarkan:
   ```bash
   iconv -f UTF-8 -t ASCII//TRANSLIT -c input.txt -o output.txt
   ```

4. Menukar encoding dan mencetak output ke terminal:
   ```bash
   iconv -f UTF-8 -t UTF-16 input.txt
   ```

## Tips
- Sentiasa buat salinan fail asal sebelum melakukan penukaran untuk mengelakkan kehilangan data.
- Uji penukaran dengan fail kecil terlebih dahulu untuk memastikan hasilnya seperti yang diharapkan.
- Gunakan pilihan `-c` jika anda tidak mahu melihat amaran tentang karakter yang tidak boleh ditukarkan.