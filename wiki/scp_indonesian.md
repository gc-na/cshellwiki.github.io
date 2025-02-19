# [Sistem Operasi] C Shell (csh) scp Penggunaan: Menyalin file secara aman antar host

## Overview
Perintah `scp` (Secure Copy Protocol) digunakan untuk menyalin file atau direktori antara komputer secara aman melalui protokol SSH. Ini memungkinkan pengguna untuk mentransfer data dengan enkripsi, menjaga keamanan informasi yang dikirimkan.

## Usage
Berikut adalah sintaks dasar dari perintah `scp`:

```
scp [options] [source] [destination]
```

## Common Options
- `-r`: Menyalin direktori secara rekursif.
- `-P`: Menentukan port SSH yang akan digunakan (perhatikan huruf besar).
- `-i`: Menentukan file kunci identitas untuk otentikasi.
- `-v`: Menampilkan informasi lebih detail tentang proses transfer (verbose).

## Common Examples
Berikut adalah beberapa contoh penggunaan `scp`:

1. Menyalin file dari lokal ke remote server:
   ```bash
   scp file.txt user@remote_host:/path/to/destination
   ```

2. Menyalin file dari remote server ke lokal:
   ```bash
   scp user@remote_host:/path/to/file.txt /local/path
   ```

3. Menyalin direktori secara rekursif:
   ```bash
   scp -r /local/directory user@remote_host:/path/to/destination
   ```

4. Menyalin file menggunakan port SSH yang berbeda:
   ```bash
   scp -P 2222 file.txt user@remote_host:/path/to/destination
   ```

## Tips
- Selalu gunakan opsi `-v` saat mengalami masalah untuk mendapatkan informasi lebih lanjut tentang transfer.
- Pastikan Anda memiliki izin yang tepat untuk mengakses file dan direktori yang ingin Anda salin.
- Pertimbangkan untuk menggunakan kunci SSH untuk otentikasi yang lebih aman daripada menggunakan kata sandi.