# [Linux] Bash env Penggunaan: Mengurus Persekitaran

## Overview
Perintah `env` digunakan untuk mengurus dan memaparkan pembolehubah persekitaran dalam sistem Linux. Ia membolehkan pengguna untuk menjalankan program dengan pembolehubah persekitaran tertentu tanpa mengubah persekitaran semasa.

## Usage
Sintaks asas untuk perintah `env` adalah seperti berikut:

```
env [options] [arguments]
```

## Common Options
- `-i`: Menjalankan perintah dalam persekitaran kosong, tanpa pembolehubah persekitaran yang sedia ada.
- `-u NAME`: Menghapuskan pembolehubah persekitaran yang dinamakan `NAME`.
- `VAR=VALUE`: Menetapkan pembolehubah persekitaran baru untuk perintah yang akan dijalankan.

## Common Examples
1. **Menampilkan semua pembolehubah persekitaran:**
   ```bash
   env
   ```

2. **Menjalankan perintah dengan pembolehubah persekitaran baru:**
   ```bash
   env VAR1=value1 VAR2=value2 command
   ```

3. **Menghapuskan pembolehubah persekitaran tertentu:**
   ```bash
   env -u VAR1 command
   ```

4. **Menjalankan perintah dalam persekitaran kosong:**
   ```bash
   env -i command
   ```

## Tips
- Gunakan `env` untuk menguji skrip atau perintah dalam persekitaran yang bersih dengan pilihan `-i`.
- Sentiasa semak pembolehubah persekitaran yang ada sebelum menjalankan perintah untuk memastikan tiada konflik.
- Untuk menetapkan pembolehubah persekitaran yang hanya digunakan dalam satu perintah, gunakan sintaks `VAR=value command` untuk mengelakkan perubahan pada persekitaran global.