# [Linux] Bash groupmod Penggunaan: Mengubah atribut grup

## Overview
Perintah `groupmod` digunakan untuk mengubah atribut dari grup yang ada di sistem Linux. Dengan menggunakan perintah ini, Anda dapat mengubah nama grup, GID (Group ID), dan atribut lainnya.

## Usage
Berikut adalah sintaks dasar dari perintah `groupmod`:

```bash
groupmod [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan `groupmod`:

- `-n, --new-name NEW_GROUP`: Mengubah nama grup menjadi `NEW_GROUP`.
- `-g, --gid GID`: Mengubah GID grup menjadi nilai yang ditentukan.
- `-h, --help`: Menampilkan bantuan penggunaan perintah ini.

## Common Examples
Berikut adalah beberapa contoh penggunaan `groupmod`:

1. **Mengubah nama grup**:
   ```bash
   groupmod -n nama_baru nama_lama
   ```

2. **Mengubah GID grup**:
   ```bash
   groupmod -g 1001 nama_grup
   ```

3. **Mengubah nama dan GID grup sekaligus**:
   ```bash
   groupmod -n nama_baru -g 1002 nama_lama
   ```

## Tips
- Pastikan Anda memiliki hak akses yang cukup (seperti pengguna root) untuk menjalankan perintah `groupmod`.
- Selalu periksa grup yang ada sebelum melakukan perubahan untuk menghindari konflik nama.
- Gunakan opsi `--help` untuk mendapatkan informasi lebih lanjut tentang penggunaan perintah ini jika diperlukan.