# [Linux] Bash psql Penggunaan: Mengakses dan mengurus pangkalan data PostgreSQL

## Overview
Perintah `psql` adalah alat baris perintah untuk berinteraksi dengan pangkalan data PostgreSQL. Ia membolehkan pengguna untuk menjalankan arahan SQL, mengurus pangkalan data, dan melaksanakan skrip SQL dengan mudah.

## Usage
Sintaks asas untuk menggunakan `psql` adalah seperti berikut:

```bash
psql [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan umum yang boleh digunakan dengan `psql`:

- `-h`: Menentukan hos pangkalan data.
- `-U`: Menentukan nama pengguna untuk sambungan.
- `-d`: Menentukan nama pangkalan data untuk disambungkan.
- `-f`: Menjalankan arahan SQL dari fail.
- `-c`: Menjalankan arahan SQL yang diberikan sebagai argumen.

## Common Examples
Berikut adalah beberapa contoh praktikal menggunakan `psql`:

1. **Menyambung ke pangkalan data secara interaktif:**
   ```bash
   psql -U username -d databasename
   ```

2. **Menjalankan arahan SQL dari fail:**
   ```bash
   psql -U username -d databasename -f /path/to/file.sql
   ```

3. **Menjalankan arahan SQL secara langsung:**
   ```bash
   psql -U username -d databasename -c "SELECT * FROM tablename;"
   ```

4. **Menyambung ke pangkalan data di hos tertentu:**
   ```bash
   psql -h hostname -U username -d databasename
   ```

## Tips
- Sentiasa gunakan nama pengguna dan kata laluan yang selamat untuk sambungan ke pangkalan data.
- Gunakan pilihan `-f` untuk menjalankan skrip SQL yang panjang untuk mengelakkan kesilapan semasa menaip arahan secara manual.
- Untuk mendapatkan bantuan lanjut, gunakan arahan `\?` selepas menyambung ke `psql` untuk melihat senarai arahan dan pilihan yang tersedia.