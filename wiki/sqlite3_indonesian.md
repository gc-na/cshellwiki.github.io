# [Sistem Operasi] C Shell (csh) sqlite3 Penggunaan: Mengelola Basis Data SQLite

## Overview
Perintah `sqlite3` digunakan untuk mengakses dan mengelola basis data SQLite. Dengan perintah ini, pengguna dapat menjalankan kueri SQL, membuat tabel, dan melakukan berbagai operasi pada data yang tersimpan dalam file basis data SQLite.

## Usage
Berikut adalah sintaks dasar dari perintah `sqlite3`:

```csh
sqlite3 [options] [arguments]
```

## Common Options
- `-help`: Menampilkan bantuan dan informasi tentang penggunaan perintah.
- `-version`: Menampilkan versi SQLite yang sedang digunakan.
- `-init <file>`: Menjalankan perintah SQL dari file yang ditentukan saat memulai.
- `-batch`: Menjalankan dalam mode batch, cocok untuk skrip otomatis tanpa interaksi pengguna.

## Common Examples
Berikut adalah beberapa contoh penggunaan `sqlite3`:

1. **Membuka basis data SQLite**:
   ```csh
   sqlite3 mydatabase.db
   ```

2. **Menjalankan kueri SQL untuk membuat tabel**:
   ```csh
   sqlite3 mydatabase.db "CREATE TABLE users (id INTEGER PRIMARY KEY, name TEXT);"
   ```

3. **Menambahkan data ke tabel**:
   ```csh
   sqlite3 mydatabase.db "INSERT INTO users (name) VALUES ('Alice');"
   ```

4. **Mengambil data dari tabel**:
   ```csh
   sqlite3 mydatabase.db "SELECT * FROM users;"
   ```

5. **Menjalankan skrip SQL dari file**:
   ```csh
   sqlite3 mydatabase.db < script.sql
   ```

## Tips
- Selalu buat cadangan basis data sebelum melakukan operasi yang dapat mengubah data secara permanen.
- Gunakan mode batch saat menjalankan skrip untuk menghindari interaksi manual yang tidak perlu.
- Manfaatkan opsi `-init` untuk menjalankan skrip awal yang diperlukan saat membuka basis data.