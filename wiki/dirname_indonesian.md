# [Linux] Bash dirname Penggunaan: Mengambil nama direktori dari jalur file

## Overview
Perintah `dirname` digunakan untuk mengambil nama direktori dari jalur file yang diberikan. Ini berguna ketika Anda ingin memisahkan nama file dari jalur direktori lengkapnya.

## Usage
Sintaks dasar dari perintah `dirname` adalah sebagai berikut:

```bash
dirname [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum untuk `dirname` beserta penjelasannya:

- `-z` : Menggunakan pemisah null untuk input dan output.
- `--help` : Menampilkan bantuan penggunaan perintah.
- `--version` : Menampilkan versi dari perintah `dirname`.

## Common Examples
Berikut adalah beberapa contoh praktis penggunaan `dirname`:

1. Mengambil nama direktori dari jalur file:
   ```bash
   dirname /home/user/documents/file.txt
   ```
   Output:
   ```
   /home/user/documents
   ```

2. Mengambil nama direktori dari jalur file relatif:
   ```bash
   dirname ./folder/file.txt
   ```
   Output:
   ```
   ./folder
   ```

3. Menggunakan `dirname` dalam skrip untuk mendapatkan direktori dari variabel:
   ```bash
   FILE_PATH="/usr/local/bin/script.sh"
   DIR_NAME=$(dirname "$FILE_PATH")
   echo $DIR_NAME
   ```
   Output:
   ```
   /usr/local/bin
   ```

## Tips
- Gunakan `dirname` dalam kombinasi dengan perintah lain seperti `basename` untuk memanipulasi jalur file secara lebih efisien.
- Pastikan untuk menggunakan tanda kutip pada jalur file yang mengandung spasi untuk menghindari kesalahan.
- Anda dapat menggunakan `dirname` dalam skrip shell untuk secara otomatis mendapatkan jalur direktori dari file yang sedang diproses.