# [Linux] Bash vigr Penggunaan: Mengedit fail konfigurasi vim

## Overview
Perintah `vigr` adalah alat yang digunakan untuk mengedit fail konfigurasi sistem yang berkaitan dengan pengguna dan kumpulan, seperti `/etc/group` dan `/etc/passwd`. Ia membuka fail tersebut dalam editor teks `vim`, memastikan bahawa fail tersebut tidak diubah suai oleh proses lain semasa pengeditan.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `vigr`:

```bash
vigr [options] [arguments]
```

## Common Options
- `-h`, `--help`: Menunjukkan bantuan dan maklumat penggunaan.
- `-s`, `--safe`: Membuka fail dalam mod selamat, menghalang pengeditan jika terdapat kesilapan dalam fail.
- `-o`, `--editor`: Menentukan editor lain yang ingin digunakan selain `vim`.

## Common Examples
Berikut adalah beberapa contoh penggunaan `vigr`:

1. Mengedit fail `/etc/group`:
   ```bash
   sudo vigr /etc/group
   ```

2. Mengedit fail `/etc/passwd` dengan mod selamat:
   ```bash
   sudo vigr -s /etc/passwd
   ```

3. Menggunakan editor lain, seperti `nano`:
   ```bash
   sudo vigr -o nano /etc/group
   ```

## Tips
- Sentiasa gunakan `sudo` untuk mengedit fail sistem agar anda mempunyai keizinan yang diperlukan.
- Pastikan untuk menyemak kesilapan dalam fail selepas pengeditan, terutamanya jika menggunakan mod selamat.
- Jika anda tidak biasa dengan `vim`, pertimbangkan untuk menggunakan pilihan `-o` untuk menggunakan editor yang lebih mesra pengguna.