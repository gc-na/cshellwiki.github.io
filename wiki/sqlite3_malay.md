# [Linux] Bash sqlite3 Penggunaan: Mengurus pangkalan data SQLite

## Overview
Perintah `sqlite3` digunakan untuk mengakses dan mengurus pangkalan data SQLite. Ia membolehkan pengguna untuk menjalankan arahan SQL, mencipta dan mengubah suai pangkalan data, serta melaksanakan pelbagai operasi lain yang berkaitan dengan pengurusan data.

## Usage
Sintaks asas untuk menggunakan `sqlite3` adalah seperti berikut:

```bash
sqlite3 [options] [arguments]
```

## Common Options
- `-help`: Menunjukkan bantuan dan senarai pilihan yang tersedia.
- `-version`: Menunjukkan versi SQLite yang sedang digunakan.
- `-init <file>`: Memuatkan fail SQL semasa memulakan sesi sqlite3.
- `-batch`: Mengaktifkan mod batch, membolehkan pelaksanaan arahan tanpa interaksi pengguna.

## Common Examples
Berikut adalah beberapa contoh penggunaan `sqlite3`:

1. **Mencipta pangkalan data baru:**
   ```bash
   sqlite3 mydatabase.db
   ```

2. **Menjalankan arahan SQL dari fail:**
   ```bash
   sqlite3 mydatabase.db < script.sql
   ```

3. **Menjalankan arahan SQL secara langsung:**
   ```bash
   sqlite3 mydatabase.db "CREATE TABLE users (id INTEGER PRIMARY KEY, name TEXT);"
   ```

4. **Mengeluarkan data dari jadual:**
   ```bash
   sqlite3 mydatabase.db "SELECT * FROM users;"
   ```

5. **Mengeluarkan hasil dalam format CSV:**
   ```bash
   sqlite3 -header -csv mydatabase.db "SELECT * FROM users;" > output.csv
   ```

## Tips
- Sentiasa buat salinan sandaran pangkalan data sebelum melakukan operasi yang merosakkan.
- Gunakan mod `-batch` untuk menjalankan skrip SQL secara automatik tanpa perlu interaksi.
- Manfaatkan pilihan `-init` untuk memuatkan konfigurasi atau arahan awal setiap kali anda memulakan sesi sqlite3.