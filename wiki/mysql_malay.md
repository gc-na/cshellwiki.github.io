# [Linux] Bash mysql Penggunaan: Mengurus pangkalan data MySQL

## Overview
Perintah `mysql` adalah alat baris perintah yang digunakan untuk berinteraksi dengan pangkalan data MySQL. Ia membolehkan pengguna untuk menjalankan kueri SQL, menguruskan pangkalan data, dan melakukan pelbagai operasi lain berkaitan dengan pengurusan data.

## Usage
Sintaks asas untuk menggunakan perintah `mysql` adalah seperti berikut:

```bash
mysql [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa yang boleh digunakan dengan perintah `mysql`:

- `-u` : Menentukan nama pengguna untuk log masuk ke MySQL.
- `-p` : Meminta kata laluan untuk pengguna yang ditentukan.
- `-h` : Menentukan hos pelayan MySQL (default adalah `localhost`).
- `-D` : Menentukan pangkalan data yang ingin digunakan selepas log masuk.
- `-e` : Menjalankan arahan SQL yang diberikan dan keluar.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `mysql`:

1. **Log masuk ke MySQL tanpa pangkalan data tertentu:**
   ```bash
   mysql -u username -p
   ```

2. **Log masuk ke MySQL dan memilih pangkalan data tertentu:**
   ```bash
   mysql -u username -p -D database_name
   ```

3. **Menjalankan arahan SQL secara langsung:**
   ```bash
   mysql -u username -p -e "SHOW DATABASES;"
   ```

4. **Mengeksport pangkalan data ke dalam fail SQL:**
   ```bash
   mysqldump -u username -p database_name > backup.sql
   ```

5. **Mengimport fail SQL ke dalam pangkalan data:**
   ```bash
   mysql -u username -p database_name < backup.sql
   ```

## Tips
- Sentiasa gunakan kata laluan yang kuat untuk melindungi akses ke pangkalan data anda.
- Gunakan pilihan `-e` untuk menjalankan arahan SQL secara langsung tanpa perlu memasuki sesi interaktif.
- Untuk mengelakkan kehilangan data, lakukan sandaran pangkalan data secara berkala menggunakan `mysqldump`.
- Jika anda sering menggunakan pangkalan data yang sama, pertimbangkan untuk membuat fail konfigurasi `.my.cnf` untuk menyimpan maklumat log masuk.