# [Linux] Bash id penggunaan: [menunjukkan identiti pengguna]

## Overview
Perintah `id` dalam Bash digunakan untuk menunjukkan maklumat identiti pengguna semasa, termasuk UID (User ID), GID (Group ID), dan kumpulan yang dimiliki oleh pengguna tersebut. Ini berguna untuk memahami hak akses dan keahlian pengguna dalam sistem.

## Usage
Sintaks asas untuk perintah `id` adalah seperti berikut:

```
id [options] [arguments]
```

## Common Options
- `-u`: Menunjukkan UID pengguna semasa.
- `-g`: Menunjukkan GID kumpulan utama pengguna semasa.
- `-G`: Menunjukkan semua GID yang dimiliki oleh pengguna.
- `-n`: Menunjukkan nama pengguna atau nama kumpulan bukannya ID.
- `-r`: Menunjukkan ID yang sebenar (real ID) pengguna atau kumpulan.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `id`:

1. **Menunjukkan maklumat pengguna semasa:**
   ```bash
   id
   ```

2. **Menunjukkan UID pengguna semasa:**
   ```bash
   id -u
   ```

3. **Menunjukkan GID kumpulan utama pengguna semasa:**
   ```bash
   id -g
   ```

4. **Menunjukkan semua GID yang dimiliki oleh pengguna semasa:**
   ```bash
   id -G
   ```

5. **Menunjukkan nama pengguna berdasarkan UID:**
   ```bash
   id -n -u
   ```

## Tips
- Gunakan `id` tanpa sebarang pilihan untuk mendapatkan maklumat lengkap tentang pengguna semasa.
- Jika anda ingin mengetahui maklumat pengguna lain, anda boleh menambah nama pengguna sebagai argumen, contohnya: `id username`.
- Perintah ini sangat berguna dalam skrip untuk memeriksa keahlian pengguna sebelum melaksanakan tugas tertentu.