# [Linux] Bash screen penggunaan: Mengelola sesi terminal

## Overview
Perintah `screen` adalah alat yang memungkinkan pengguna untuk menjalankan beberapa sesi terminal dalam satu jendela. Dengan `screen`, Anda dapat menjalankan proses di latar belakang, terputus dari sesi, dan kemudian terhubung kembali tanpa kehilangan pekerjaan yang sedang berlangsung.

## Usage
Sintaks dasar dari perintah `screen` adalah sebagai berikut:

```bash
screen [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang sering digunakan dengan perintah `screen`:

- `-S [nama]`: Menentukan nama sesi untuk memudahkan pengelolaan.
- `-d -r`: Memisahkan sesi yang sedang berjalan dan menghubungkannya kembali.
- `-list`: Menampilkan daftar sesi `screen` yang sedang berjalan.
- `-h [jumlah]`: Menentukan jumlah baris riwayat yang akan disimpan.

## Common Examples
Berikut adalah beberapa contoh penggunaan `screen`:

1. **Memulai sesi baru**:
   ```bash
   screen
   ```

2. **Memulai sesi baru dengan nama**:
   ```bash
   screen -S mysession
   ```

3. **Melihat daftar sesi yang sedang berjalan**:
   ```bash
   screen -list
   ```

4. **Menghubungkan kembali ke sesi yang terputus**:
   ```bash
   screen -r mysession
   ```

5. **Memisahkan sesi yang sedang berjalan**:
   Tekan `Ctrl + A`, lalu `D`.

## Tips
- Selalu beri nama pada sesi Anda dengan opsi `-S` agar lebih mudah dikenali.
- Gunakan perintah `screen -ls` untuk memeriksa sesi yang sedang berjalan sebelum memulai sesi baru.
- Jika Anda sering bekerja dengan aplikasi yang memerlukan waktu lama, pertimbangkan untuk menggunakan `screen` agar tidak kehilangan kemajuan saat terputus dari koneksi.