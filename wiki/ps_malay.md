# [Linux] Bash ps Penggunaan: Menunjukkan proses yang sedang berjalan

## Overview
Perintah `ps` digunakan dalam sistem operasi Linux untuk memaparkan maklumat tentang proses yang sedang berjalan. Ia memberikan gambaran ringkas mengenai proses-proses ini, termasuk ID proses (PID), penggunaan CPU, dan memori.

## Usage
Sintaks asas untuk perintah `ps` adalah seperti berikut:

```
ps [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk `ps` beserta penjelasan ringkas:

- `-e` atau `-A`: Menunjukkan semua proses yang sedang berjalan.
- `-f`: Menunjukkan maklumat proses dalam format penuh.
- `-u [user]`: Menunjukkan proses yang dimiliki oleh pengguna tertentu.
- `-aux`: Menunjukkan semua proses dengan maklumat terperinci.
- `--sort`: Mengatur output berdasarkan kriteria tertentu, seperti penggunaan CPU atau memori.

## Common Examples
Berikut adalah beberapa contoh penggunaan `ps`:

1. Menunjukkan semua proses yang sedang berjalan:
   ```bash
   ps -e
   ```

2. Menunjukkan proses dalam format penuh:
   ```bash
   ps -f
   ```

3. Menunjukkan proses yang dimiliki oleh pengguna tertentu:
   ```bash
   ps -u username
   ```

4. Menunjukkan semua proses dengan maklumat terperinci:
   ```bash
   ps aux
   ```

5. Mengatur output berdasarkan penggunaan CPU:
   ```bash
   ps aux --sort=-%cpu
   ```

## Tips
- Gunakan `ps aux` untuk mendapatkan maklumat terperinci tentang semua proses yang sedang berjalan.
- Kombinasikan `ps` dengan `grep` untuk mencari proses tertentu. Contohnya:
  ```bash
  ps aux | grep firefox
  ```
- Untuk memantau proses secara berterusan, pertimbangkan untuk menggunakan perintah `top` atau `htop` sebagai alternatif.