# [Sistem Operasi] C Shell (csh) top Penggunaan: Menampilkan proses yang berjalan

## Overview
Perintah `top` digunakan untuk menampilkan informasi tentang proses yang sedang berjalan di sistem. Ini memberikan tampilan real-time dari penggunaan CPU, memori, dan informasi penting lainnya tentang proses yang aktif.

## Usage
Berikut adalah sintaks dasar dari perintah `top`:

```csh
top [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan perintah `top`:

- `-d <seconds>`: Menentukan interval pembaruan dalam detik.
- `-p <pid>`: Menampilkan hanya proses dengan ID tertentu.
- `-u <username>`: Menampilkan proses yang dijalankan oleh pengguna tertentu.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `top`:

1. Menjalankan `top` dengan pembaruan setiap 5 detik:
   ```csh
   top -d 5
   ```

2. Menampilkan proses untuk pengguna tertentu:
   ```csh
   top -u username
   ```

3. Menampilkan informasi hanya untuk proses dengan ID 1234:
   ```csh
   top -p 1234
   ```

## Tips
- Gunakan opsi `-d` untuk menyesuaikan frekuensi pembaruan tampilan agar sesuai dengan kebutuhan Anda.
- Tekan `h` saat berada di dalam tampilan `top` untuk melihat bantuan dan daftar pintasan keyboard.
- Untuk menghentikan proses tertentu, Anda dapat menggunakan opsi `k` di dalam antarmuka `top` dan memasukkan ID proses yang ingin dihentikan.