# [Linux] Bash source Penggunaan: Menjalankan skrip di shell saat ini

## Overview
Perintah `source` dalam Bash digunakan untuk menjalankan skrip shell dalam konteks shell saat ini. Ini berarti bahwa setiap perubahan yang dilakukan oleh skrip, seperti pengaturan variabel atau fungsi, akan tetap ada setelah skrip selesai dijalankan.

## Usage
Sintaks dasar dari perintah `source` adalah sebagai berikut:

```
source [options] [arguments]
```

## Common Options
- `-h`, `--help`: Menampilkan bantuan mengenai penggunaan perintah `source`.
- `-V`, `--version`: Menampilkan versi dari shell yang digunakan.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `source`:

1. Menjalankan skrip bernama `myscript.sh`:
   ```bash
   source myscript.sh
   ```

2. Menggunakan titik (.) sebagai alternatif untuk `source`:
   ```bash
   . myscript.sh
   ```

3. Menjalankan skrip yang mengatur variabel lingkungan:
   ```bash
   source setenv.sh
   ```

4. Memuat fungsi dari skrip ke dalam shell saat ini:
   ```bash
   source functions.sh
   ```

## Tips
- Gunakan `source` untuk memuat skrip yang sering digunakan agar tidak perlu mengeksekusi ulang setiap kali.
- Pastikan skrip yang akan dijalankan memiliki izin eksekusi yang sesuai.
- Jika skrip mengubah variabel, pastikan untuk memeriksa nilai variabel tersebut setelah menjalankan `source` untuk memastikan perubahan diterapkan.