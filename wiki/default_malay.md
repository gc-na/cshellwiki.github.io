# [Linux] Bash default penggunaan: Mengurus proses

## Overview
Perintah `default` dalam Bash digunakan untuk mengurus dan mengendalikan proses yang sedang berjalan dalam sistem. Ia membolehkan pengguna untuk memantau, menghentikan, dan mengubah keutamaan proses.

## Usage
Berikut adalah sintaks asas untuk perintah `default`:

```bash
default [options] [arguments]
```

## Common Options
- `-h`, `--help`: Menunjukkan bantuan dan maklumat tentang cara menggunakan perintah ini.
- `-v`, `--version`: Menunjukkan versi perintah `default`.
- `-p`, `--pid`: Mengambil ID proses tertentu untuk pengendalian.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `default`:

1. **Menunjukkan semua proses yang sedang berjalan:**
   ```bash
   default -p
   ```

2. **Menghentikan proses dengan ID tertentu:**
   ```bash
   default -p 1234
   ```

3. **Mengubah keutamaan proses:**
   ```bash
   default -p 1234 --priority 10
   ```

## Tips
- Sentiasa semak ID proses sebelum menghentikan atau mengubah keutamaan untuk mengelakkan menghentikan proses penting.
- Gunakan pilihan `--help` untuk mendapatkan maklumat lanjut tentang pilihan yang tersedia.
- Amalkan penggunaan `default` dalam skrip automasi untuk mengurus proses secara efisien.