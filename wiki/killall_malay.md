# [Linux] Bash killall Penggunaan: Menghentikan proses berdasarkan nama

## Overview
Perintah `killall` dalam Bash digunakan untuk menghentikan semua proses yang berjalan dengan nama tertentu. Ini berguna apabila anda ingin menamatkan beberapa proses yang sama tanpa perlu mencari dan menghentikan setiap satu secara manual.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `killall`:

```bash
killall [options] [arguments]
```

## Common Options
- `-u, --user <user>`: Hentikan proses yang dimiliki oleh pengguna tertentu.
- `-q, --quiet`: Jangan cetak mesej ralat jika tiada proses yang dijumpai.
- `-I, --ignore-case`: Abaikan kes apabila mencari nama proses.
- `-s, --signal <signal>`: Hantar isyarat tertentu kepada proses (contoh: `SIGTERM`, `SIGKILL`).

## Common Examples
Berikut adalah beberapa contoh penggunaan `killall`:

1. **Menghentikan semua proses dengan nama "firefox":**
   ```bash
   killall firefox
   ```

2. **Menghentikan semua proses "gedit" dengan isyarat SIGKILL:**
   ```bash
   killall -s SIGKILL gedit
   ```

3. **Menghentikan proses yang dimiliki oleh pengguna tertentu:**
   ```bash
   killall -u username process_name
   ```

4. **Menghentikan semua proses "python" tanpa mencetak mesej ralat:**
   ```bash
   killall -q python
   ```

## Tips
- Sentiasa semak nama proses yang ingin dihentikan untuk mengelakkan menghentikan proses yang salah.
- Gunakan pilihan `-q` untuk mengelakkan mesej ralat yang tidak perlu jika tiada proses yang dijumpai.
- Jika anda tidak pasti tentang proses yang sedang berjalan, gunakan `ps aux` untuk melihat senarai proses sebelum menggunakan `killall`.