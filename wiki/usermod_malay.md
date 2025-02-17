# [Linux] Bash usermod Penggunaan: Mengubah atribut pengguna

## Overview
Perintah `usermod` digunakan untuk mengubah atribut pengguna dalam sistem Linux. Ini membolehkan pentadbir sistem untuk mengubah pelbagai parameter pengguna seperti nama, kumpulan, dan hak akses.

## Usage
Sintaks asas untuk perintah `usermod` adalah seperti berikut:

```bash
usermod [options] [arguments]
```

## Common Options
- `-aG`: Menambah pengguna ke kumpulan tambahan tanpa mengeluarkannya dari kumpulan lain.
- `-d`: Mengubah direktori home pengguna.
- `-l`: Mengubah nama pengguna.
- `-s`: Mengubah shell pengguna.
- `-u`: Mengubah UID (User ID) pengguna.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `usermod`:

1. **Menambah pengguna ke kumpulan tambahan**:
   ```bash
   usermod -aG sudo username
   ```

2. **Mengubah nama pengguna**:
   ```bash
   usermod -l newusername oldusername
   ```

3. **Mengubah direktori home pengguna**:
   ```bash
   usermod -d /new/home/directory username
   ```

4. **Mengubah shell pengguna**:
   ```bash
   usermod -s /bin/bash username
   ```

5. **Mengubah UID pengguna**:
   ```bash
   usermod -u 1001 username
   ```

## Tips
- Sentiasa buat salinan sandaran fail konfigurasi sebelum membuat perubahan besar.
- Gunakan `usermod` dengan berhati-hati, terutamanya ketika mengubah nama pengguna atau UID, kerana ini boleh mempengaruhi akses kepada fail dan direktori.
- Pastikan untuk menggunakan `-aG` ketika menambah pengguna ke kumpulan tambahan untuk mengelakkan penghapusan dari kumpulan lain.