# [Linux] Bash top Penggunaan: Memantau proses sistem secara real-time

## Overview
Perintah `top` digunakan untuk menampilkan informasi tentang proses yang sedang berjalan di sistem Linux. Ini memberikan tampilan real-time dari penggunaan CPU, memori, dan informasi lainnya yang berkaitan dengan proses. Dengan `top`, pengguna dapat memantau kinerja sistem dan mengidentifikasi proses yang mungkin mempengaruhi kinerja.

## Usage
Sintaks dasar dari perintah `top` adalah sebagai berikut:
```
top [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan perintah `top`:

- `-d <delay>`: Mengatur interval pembaruan tampilan dalam detik.
- `-n <number>`: Menentukan jumlah iterasi yang akan ditampilkan sebelum keluar.
- `-u <user>`: Menampilkan hanya proses yang dimiliki oleh pengguna tertentu.
- `-p <pid>`: Menampilkan hanya proses dengan ID proses tertentu.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `top`:

1. Menjalankan `top` dengan pembaruan setiap 2 detik:
   ```bash
   top -d 2
   ```

2. Menampilkan proses yang dimiliki oleh pengguna tertentu:
   ```bash
   top -u username
   ```

3. Menjalankan `top` untuk menampilkan hanya proses dengan ID tertentu:
   ```bash
   top -p 1234
   ```

4. Menjalankan `top` dan menampilkan hanya 5 iterasi:
   ```bash
   top -n 5
   ```

## Tips
- Gunakan `Shift + M` saat berada dalam tampilan `top` untuk mengurutkan proses berdasarkan penggunaan memori.
- Tekan `q` untuk keluar dari tampilan `top` dengan cepat.
- Anda dapat menekan `h` untuk melihat bantuan dan daftar pintasan keyboard yang tersedia dalam `top`.