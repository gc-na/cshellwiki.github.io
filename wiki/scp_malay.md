# [Linux] Bash scp Penggunaan: Memindahkan fail dengan selamat

## Overview
Perintah `scp` (Secure Copy Protocol) digunakan untuk menyalin fail dan direktori antara sistem yang berbeza melalui sambungan SSH yang selamat. Ia membolehkan pengguna memindahkan data dengan cara yang selamat dan mudah.

## Usage
Sintaks asas untuk perintah `scp` adalah seperti berikut:

```
scp [options] [source] [destination]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk `scp`:

- `-r`: Menyalin direktori secara rekursif.
- `-P`: Menentukan nombor port SSH yang digunakan.
- `-i`: Menggunakan fail kunci identiti untuk pengesahan.
- `-v`: Mengaktifkan mod verbose untuk melihat maklumat lanjut tentang proses pemindahan.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `scp`:

1. Menyalin fail dari komputer tempatan ke pelayan jauh:
   ```
   scp file.txt user@remote_host:/path/to/destination/
   ```

2. Menyalin fail dari pelayan jauh ke komputer tempatan:
   ```
   scp user@remote_host:/path/to/file.txt /local/destination/
   ```

3. Menyalin direktori secara rekursif ke pelayan jauh:
   ```
   scp -r /local/directory user@remote_host:/path/to/destination/
   ```

4. Menyalin fail menggunakan port SSH yang berbeza:
   ```
   scp -P 2222 file.txt user@remote_host:/path/to/destination/
   ```

## Tips
- Sentiasa gunakan sambungan SSH yang selamat untuk memastikan keselamatan data anda.
- Gunakan pilihan `-v` untuk menyelesaikan masalah jika pemindahan gagal.
- Pastikan anda mempunyai kebenaran yang betul untuk menyalin fail ke lokasi yang dituju.