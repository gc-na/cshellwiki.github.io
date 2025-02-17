# [Linux] Bash groupmod Penggunaan: Mengubah kumpulan pengguna

## Overview
Perintah `groupmod` digunakan untuk mengubah atribut kumpulan pengguna dalam sistem Linux. Dengan perintah ini, anda boleh mengubah nama kumpulan, GID (Group ID), dan atribut lain yang berkaitan dengan kumpulan.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `groupmod`:

```bash
groupmod [options] [arguments]
```

## Common Options
- `-n, --new-name NEW_GROUP`: Menetapkan nama baru untuk kumpulan.
- `-g, --gid GID`: Menetapkan GID baru untuk kumpulan.
- `-o, --non-unique`: Membenarkan penggunaan GID yang tidak unik.

## Common Examples
Berikut adalah beberapa contoh penggunaan `groupmod`:

1. **Mengubah nama kumpulan**:
   ```bash
   groupmod -n nama_baru nama_lama
   ```

2. **Mengubah GID kumpulan**:
   ```bash
   groupmod -g 1001 nama_kumpulan
   ```

3. **Mengubah nama dan GID sekaligus**:
   ```bash
   groupmod -n nama_baru -g 1002 nama_lama
   ```

4. **Membenarkan GID tidak unik**:
   ```bash
   groupmod -o -g 1001 nama_kumpulan
   ```

## Tips
- Pastikan anda mempunyai hak akses yang diperlukan (biasanya sebagai pengguna root) untuk menjalankan perintah `groupmod`.
- Sentiasa periksa kumpulan yang ada sebelum membuat perubahan untuk mengelakkan konflik nama atau GID.
- Gunakan perintah `getent group` untuk melihat senarai kumpulan dan GID yang ada dalam sistem.