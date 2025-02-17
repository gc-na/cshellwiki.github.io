# [Linux] Bash who penggunaan: Menunjukkan pengguna yang sedang log masuk

## Overview
Perintah `who` dalam Bash digunakan untuk menampilkan senarai pengguna yang sedang log masuk ke sistem. Ia memberikan maklumat tentang sesi pengguna, termasuk nama pengguna, terminal, dan waktu log masuk.

## Usage
Berikut adalah sintaks asas untuk perintah `who`:

```
who [options] [arguments]
```

## Common Options
- `-H`, `--heading`: Menunjukkan tajuk untuk kolum output.
- `-q`, `--count`: Menunjukkan hanya nama pengguna dan jumlah pengguna yang sedang log masuk.
- `-u`, `--users`: Menunjukkan waktu terakhir pengguna aktif.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `who`:

1. **Menampilkan semua pengguna yang sedang log masuk:**
   ```bash
   who
   ```

2. **Menampilkan pengguna dengan tajuk kolum:**
   ```bash
   who -H
   ```

3. **Menampilkan hanya nama pengguna dan jumlah pengguna yang log masuk:**
   ```bash
   who -q
   ```

4. **Menampilkan pengguna dengan waktu terakhir aktif:**
   ```bash
   who -u
   ```

## Tips
- Gunakan `who -H` untuk mendapatkan output yang lebih teratur dengan tajuk kolum.
- Jika anda hanya ingin mengetahui jumlah pengguna yang sedang log masuk, gunakan `who -q` untuk maklumat yang lebih ringkas.
- Perintah `who` boleh digabungkan dengan perintah lain seperti `grep` untuk mencari pengguna tertentu. Contoh:
  ```bash
  who | grep username
  ```