# [Linux] Bash dirname Penggunaan: Mengambil nama direktori dari laluan

## Overview
Perintah `dirname` digunakan untuk mengambil nama direktori dari laluan fail yang diberikan. Ia mengembalikan bahagian laluan yang menunjukkan lokasi direktori tanpa nama fail itu sendiri.

## Usage
Sintaks asas untuk perintah `dirname` adalah seperti berikut:

```bash
dirname [options] [arguments]
```

## Common Options
- `-z`, `--zero`: Menggunakan pemisah nul untuk laluan.
- `--help`: Menunjukkan maklumat bantuan tentang perintah ini.
- `--version`: Menunjukkan versi perintah `dirname`.

## Common Examples
Berikut adalah beberapa contoh penggunaan `dirname`:

1. Mengambil nama direktori dari laluan penuh:
   ```bash
   dirname /home/user/documents/file.txt
   ```
   Output:
   ```
   /home/user/documents
   ```

2. Menggunakan `dirname` dengan laluan relatif:
   ```bash
   dirname ./folder/file.txt
   ```
   Output:
   ```
   ./folder
   ```

3. Mengambil nama direktori dari laluan dengan pemisah akhir:
   ```bash
   dirname /home/user/documents/
   ```
   Output:
   ```
   /home/user/documents
   ```

4. Menggunakan `dirname` dalam skrip:
   ```bash
   FILE_PATH="/home/user/documents/file.txt"
   DIR_NAME=$(dirname "$FILE_PATH")
   echo "Direktori: $DIR_NAME"
   ```
   Output:
   ```
   Direktori: /home/user/documents
   ```

## Tips
- Gunakan `dirname` bersama perintah lain seperti `basename` untuk memanipulasi laluan fail dengan lebih berkesan.
- Sentiasa gunakan tanda petik di sekitar laluan untuk mengelakkan masalah dengan ruang atau karakter khas.
- `dirname` berguna dalam skrip untuk mendapatkan laluan direktori bagi fail yang sedang diproses.