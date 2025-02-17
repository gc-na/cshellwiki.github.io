# [Linux] Bash mysql Penggunaan: Mengelola Basis Data MySQL

## Overview
Perintah `mysql` adalah klien baris perintah untuk mengakses dan mengelola basis data MySQL. Dengan menggunakan perintah ini, pengguna dapat melakukan berbagai operasi seperti menjalankan kueri SQL, mengelola tabel, dan mengatur pengguna dalam basis data.

## Usage
Berikut adalah sintaks dasar dari perintah `mysql`:

```bash
mysql [options] [arguments]
```

## Common Options
- `-u [username]`: Menentukan nama pengguna untuk masuk ke MySQL.
- `-p`: Meminta kata sandi untuk pengguna yang ditentukan.
- `-h [hostname]`: Menentukan nama host atau alamat IP server MySQL.
- `-D [database]`: Menentukan basis data yang akan digunakan setelah masuk.
- `-e "[query]"`: Menjalankan kueri SQL langsung dari baris perintah.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `mysql`:

1. **Masuk ke MySQL dengan pengguna dan kata sandi:**
   ```bash
   mysql -u root -p
   ```

2. **Menjalankan kueri SQL langsung:**
   ```bash
   mysql -u root -p -e "SHOW DATABASES;"
   ```

3. **Mengakses basis data tertentu setelah masuk:**
   ```bash
   mysql -u root -p -D my_database
   ```

4. **Mengimpor file SQL ke dalam basis data:**
   ```bash
   mysql -u root -p my_database < backup.sql
   ```

5. **Mengekspor basis data ke file SQL:**
   ```bash
   mysqldump -u root -p my_database > backup.sql
   ```

## Tips
- Selalu gunakan opsi `-p` untuk menjaga keamanan kata sandi Anda saat masuk ke MySQL.
- Gunakan `-e` untuk menjalankan kueri cepat tanpa masuk ke antarmuka interaktif.
- Untuk menghindari kesalahan, pastikan Anda memiliki cadangan basis data sebelum melakukan operasi yang merusak.
- Manfaatkan `mysqldump` untuk membuat cadangan basis data secara berkala.