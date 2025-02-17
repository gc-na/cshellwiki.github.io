# [Linux] Bash scp Penggunaan: Menyalin file antar sistem secara aman

## Overview
Perintah `scp` (Secure Copy Protocol) digunakan untuk menyalin file atau direktori antara sistem yang terhubung melalui jaringan dengan aman. `scp` menggunakan protokol SSH untuk transfer data, sehingga memberikan enkripsi dan keamanan saat mentransfer file.

## Usage
Sintaks dasar dari perintah `scp` adalah sebagai berikut:
```bash
scp [options] [source] [destination]
```

## Common Options
- `-r`: Menyalin direktori secara rekursif.
- `-P`: Menentukan port SSH yang digunakan (perhatikan huruf besar).
- `-i`: Menentukan file kunci identitas untuk otentikasi.
- `-v`: Menampilkan informasi verbose selama proses transfer, berguna untuk debugging.

## Common Examples
1. Menyalin file dari lokal ke server:
   ```bash
   scp file.txt user@server:/path/to/destination/
   ```

2. Menyalin file dari server ke lokal:
   ```bash
   scp user@server:/path/to/file.txt /local/destination/
   ```

3. Menyalin direktori secara rekursif:
   ```bash
   scp -r /local/directory user@server:/path/to/destination/
   ```

4. Menyalin file dengan port SSH yang berbeda:
   ```bash
   scp -P 2222 file.txt user@server:/path/to/destination/
   ```

5. Menggunakan file kunci identitas:
   ```bash
   scp -i /path/to/private_key file.txt user@server:/path/to/destination/
   ```

## Tips
- Pastikan SSH sudah terinstal dan berjalan di server tujuan.
- Gunakan opsi `-v` untuk mendapatkan informasi lebih lanjut jika terjadi kesalahan saat transfer.
- Untuk transfer file besar, pertimbangkan untuk menggunakan `rsync` yang lebih efisien dalam mentransfer file yang telah ada sebelumnya.