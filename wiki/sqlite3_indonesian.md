# [Linux] Bash sqlite3 Penggunaan: Mengelola basis data SQLite

## Overview
Perintah `sqlite3` digunakan untuk berinteraksi dengan basis data SQLite. Dengan perintah ini, pengguna dapat membuat, mengedit, dan mengelola basis data dengan menggunakan perintah SQL.

## Usage
Berikut adalah sintaks dasar dari perintah `sqlite3`:

```bash
sqlite3 [options] [arguments]
```

## Common Options
- `-help`: Menampilkan bantuan dan daftar opsi yang tersedia.
- `-version`: Menampilkan versi dari sqlite3 yang sedang digunakan.
- `-init <file>`: Menjalankan perintah SQL dari file saat memulai sqlite3.
- `-batch`: Menjalankan sqlite3 dalam mode batch, tanpa interaksi pengguna.

## Common Examples
Berikut adalah beberapa contoh penggunaan `sqlite3`:

1. **Membuat basis data baru:**
   ```bash
   sqlite3 mydatabase.db
   ```

2. **Menjalankan perintah SQL dari file:**
   ```bash
   sqlite3 mydatabase.db < script.sql
   ```

3. **Menampilkan semua tabel dalam basis data:**
   ```bash
   sqlite3 mydatabase.db ".tables"
   ```

4. **Menjalankan kueri SQL untuk mengambil data:**
   ```bash
   sqlite3 mydatabase.db "SELECT * FROM mytable;"
   ```

5. **Menghapus basis data:**
   ```bash
   rm mydatabase.db
   ```

## Tips
- Selalu buat cadangan basis data sebelum melakukan perubahan besar.
- Gunakan file `.sql` untuk menyimpan skrip SQL yang sering digunakan agar lebih mudah diakses.
- Manfaatkan mode batch untuk menjalankan skrip panjang tanpa interaksi manual.