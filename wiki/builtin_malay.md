# [Linux] Bash builtin `builtin`: Mengakses fungsi built-in Bash

## Overview
Perintah `builtin` dalam Bash digunakan untuk menjalankan perintah built-in yang ada dalam shell, tanpa mengganggu perintah lain yang mungkin mempunyai nama yang sama. Ini berguna apabila anda ingin memastikan bahawa anda menggunakan versi built-in daripada perintah luar.

## Usage
Berikut adalah sintaks asas untuk perintah `builtin`:

```
builtin [options] [arguments]
```

## Common Options
- `-p`: Menggunakan versi perintah built-in yang dipanggil tanpa mengubah nilai `PATH`.
- `-f`: Mengabaikan fungsi yang mungkin mempunyai nama yang sama.

## Common Examples

1. **Menjalankan perintah `echo` built-in**:
   ```bash
   builtin echo "Ini adalah perintah echo built-in"
   ```

2. **Menggunakan `builtin` untuk menjalankan `cd`**:
   ```bash
   builtin cd /home/user
   ```

3. **Menjalankan `type` untuk melihat jenis perintah**:
   ```bash
   builtin type echo
   ```

4. **Menggunakan `builtin` untuk menjalankan `exit`**:
   ```bash
   builtin exit 0
   ```

## Tips
- Gunakan `builtin` apabila anda ingin memastikan bahawa anda menggunakan versi built-in daripada perintah yang mungkin dipanggil dari luar.
- Perintah `builtin` sangat berguna dalam skrip untuk mengelakkan konflik dengan perintah luar yang mempunyai nama yang sama.
- Sentiasa periksa dokumentasi perintah yang anda gunakan untuk memahami perbezaan antara versi built-in dan luar.