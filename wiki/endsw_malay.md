# [Linux] Bash endsw penggunaan: Menamatkan proses

## Overview
Perintah `endsw` dalam Bash digunakan untuk menamatkan proses yang sedang berjalan. Ia membolehkan pengguna untuk menghentikan proses tertentu dengan mudah tanpa perlu menutup terminal atau sesi yang sedang aktif.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `endsw`:

```bash
endsw [options] [arguments]
```

## Common Options
- `-p` : Menamatkan proses berdasarkan ID proses (PID).
- `-n` : Menamatkan proses berdasarkan nama proses.
- `-f` : Memaksa penamatan proses walaupun ia tidak responsif.

## Common Examples
Berikut adalah beberapa contoh penggunaan `endsw`:

1. Menamatkan proses berdasarkan ID proses:
   ```bash
   endsw -p 1234
   ```

2. Menamatkan proses berdasarkan nama proses:
   ```bash
   endsw -n my_process
   ```

3. Memaksa penamatan proses yang tidak responsif:
   ```bash
   endsw -f -n unresponsive_process
   ```

## Tips
- Sentiasa semak ID proses sebelum menggunakan `endsw` untuk memastikan anda menamatkan proses yang betul.
- Gunakan pilihan `-f` dengan berhati-hati, kerana ia akan menamatkan proses tanpa memberi peluang untuk menyimpan kerja yang belum disimpan.
- Jika anda tidak pasti tentang nama proses, gunakan perintah `ps` untuk menyenaraikan semua proses yang sedang berjalan sebelum menggunakan `endsw`.