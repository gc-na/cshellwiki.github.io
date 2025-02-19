# [Sistem Operasi] C Shell (csh) iotop: Memantau penggunaan I/O oleh proses

## Overview
Perintah `iotop` digunakan untuk memantau penggunaan input/output (I/O) oleh proses yang sedang berjalan di sistem. Dengan `iotop`, pengguna dapat melihat proses mana yang menggunakan I/O paling banyak, yang sangat berguna untuk mendiagnosis masalah kinerja.

## Usage
Berikut adalah sintaks dasar dari perintah `iotop`:

```bash
iotop [options] [arguments]
```

## Common Options
- `-o`, `--only`: Menampilkan hanya proses yang sedang melakukan I/O.
- `-b`, `--batch`: Menjalankan `iotop` dalam mode batch, berguna untuk pengalihan output.
- `-d`, `--delay`: Mengatur interval pembaruan dalam detik (default adalah 1 detik).
- `-p`, `--pid`: Menampilkan hanya proses dengan ID tertentu.

## Common Examples
Berikut adalah beberapa contoh penggunaan `iotop`:

1. Menjalankan `iotop` untuk melihat semua proses yang menggunakan I/O:
   ```bash
   iotop
   ```

2. Menampilkan hanya proses yang sedang melakukan I/O:
   ```bash
   iotop -o
   ```

3. Menjalankan `iotop` dalam mode batch dengan pembaruan setiap 2 detik:
   ```bash
   iotop -b -d 2
   ```

4. Menampilkan informasi I/O untuk proses dengan ID tertentu, misalnya ID 1234:
   ```bash
   iotop -p 1234
   ```

## Tips
- Gunakan opsi `-o` untuk fokus pada proses yang aktif menggunakan I/O, sehingga lebih mudah untuk mendiagnosis masalah.
- Jalankan `iotop` dengan hak akses root untuk mendapatkan informasi yang lebih lengkap tentang semua proses.
- Pertimbangkan untuk menggunakan mode batch saat ingin menyimpan output ke file untuk analisis lebih lanjut.