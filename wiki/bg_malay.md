# [Linux] Bash bg Penggunaan: Menghantar proses ke latar belakang

## Overview
Perintah `bg` dalam Bash digunakan untuk menghantar proses yang sedang berjalan ke latar belakang. Ini membolehkan pengguna untuk meneruskan kerja lain di terminal tanpa menghentikan proses yang sedang berjalan.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `bg`:

```bash
bg [options] [arguments]
```

## Common Options
- `job_spec`: Menentukan proses yang ingin dihantar ke latar belakang. Ini biasanya ditunjukkan dengan nombor pekerjaan (job number) yang boleh dilihat menggunakan perintah `jobs`.
- `-n`: Menghantar proses ke latar belakang tanpa mengeluarkan output ke terminal.

## Common Examples

1. **Menghantar proses ke latar belakang**
   Jika anda mempunyai proses yang sedang berjalan (contohnya, `sleep 100`), anda boleh menghantarnya ke latar belakang dengan:
   ```bash
   Ctrl + Z  # Untuk menghentikan proses
   bg %1     # Menghantar proses pertama ke latar belakang
   ```

2. **Menghantar proses ke latar belakang tanpa output**
   Untuk menghantar proses ke latar belakang tanpa output ke terminal, gunakan:
   ```bash
   bg -n %1
   ```

3. **Melihat semua proses latar belakang**
   Untuk melihat semua proses yang sedang berjalan di latar belakang, gunakan:
   ```bash
   jobs
   ```

## Tips
- Sentiasa semak status proses latar belakang dengan menggunakan perintah `jobs` untuk memastikan semuanya berjalan lancar.
- Gunakan `fg` untuk membawa proses yang dihantar ke latar belakang kembali ke latar depan jika perlu.
- Pastikan untuk menyimpan kerja anda sebelum menghantar proses ke latar belakang, terutamanya jika ia melibatkan pengeditan fail.