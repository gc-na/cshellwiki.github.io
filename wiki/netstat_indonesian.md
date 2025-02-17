# [Linux] Bash netstat Penggunaan: Menampilkan koneksi jaringan

## Overview
Perintah `netstat` digunakan untuk menampilkan informasi tentang koneksi jaringan, tabel routing, statistik antarmuka, dan informasi lainnya yang berkaitan dengan jaringan. Ini sangat berguna untuk mendiagnosis masalah jaringan dan memantau aktivitas jaringan di sistem.

## Usage
Sintaks dasar dari perintah `netstat` adalah sebagai berikut:

```bash
netstat [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan perintah `netstat`:

- `-a`: Menampilkan semua koneksi dan port yang mendengarkan.
- `-t`: Menampilkan koneksi TCP.
- `-u`: Menampilkan koneksi UDP.
- `-n`: Menampilkan alamat dan nomor port dalam format numerik.
- `-l`: Menampilkan hanya port yang sedang mendengarkan.
- `-p`: Menampilkan proses yang menggunakan koneksi.

## Common Examples
Berikut adalah beberapa contoh penggunaan `netstat`:

1. Menampilkan semua koneksi dan port yang mendengarkan:
   ```bash
   netstat -a
   ```

2. Menampilkan hanya koneksi TCP:
   ```bash
   netstat -t
   ```

3. Menampilkan koneksi UDP dengan alamat dan port dalam format numerik:
   ```bash
   netstat -un
   ```

4. Menampilkan semua port yang sedang mendengarkan:
   ```bash
   netstat -l
   ```

5. Menampilkan koneksi beserta proses yang menggunakannya:
   ```bash
   netstat -p
   ```

## Tips
- Gunakan opsi `-n` untuk mempercepat output dengan menghindari resolusi nama host.
- Kombinasikan beberapa opsi untuk mendapatkan informasi yang lebih spesifik, misalnya `netstat -tunlp` untuk menampilkan semua koneksi TCP dan UDP beserta prosesnya.
- Pertimbangkan untuk menggunakan `netstat` bersama dengan perintah lain seperti `grep` untuk menyaring hasil yang relevan.