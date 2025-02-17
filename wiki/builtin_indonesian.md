# [Linux] Bash builtin : Menjalankan perintah shell internal

## Overview
Perintah `builtin` dalam Bash digunakan untuk menjalankan perintah internal yang sudah ada di shell, alih-alih menjalankan perintah eksternal yang mungkin memiliki nama yang sama. Ini berguna untuk memastikan bahwa Anda menggunakan versi perintah yang disediakan oleh shell.

## Usage
Berikut adalah sintaks dasar untuk perintah `builtin`:

```
builtin [options] [arguments]
```

## Common Options
- `-p`: Menggunakan versi perintah yang terdaftar dalam PATH.
- `-f`: Mengabaikan fungsi yang ada dan memanggil perintah built-in.

## Common Examples

1. **Menjalankan perintah `echo` sebagai built-in:**
   ```bash
   builtin echo "Ini adalah perintah echo built-in"
   ```

2. **Menjalankan perintah `cd` untuk memastikan menggunakan built-in:**
   ```bash
   builtin cd /path/to/directory
   ```

3. **Menggunakan opsi `-p` untuk menjalankan perintah `type`:**
   ```bash
   builtin -p type echo
   ```

4. **Mengabaikan fungsi dan menjalankan perintah `exit`:**
   ```bash
   function exit { echo "Ini adalah fungsi exit"; }
   builtin exit
   ```

## Tips
- Gunakan `builtin` saat Anda ingin memastikan bahwa Anda menjalankan perintah internal Bash, terutama jika ada konflik dengan perintah eksternal.
- Perhatikan bahwa tidak semua perintah memiliki versi built-in, jadi pastikan untuk memeriksa dokumentasi jika Anda tidak yakin.
- Gunakan opsi `-f` dengan hati-hati, karena dapat mengabaikan fungsi yang mungkin Anda butuhkan.