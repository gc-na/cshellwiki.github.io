# [Linux] Bash iotop Penggunaan: Memantau penggunaan I/O disk oleh proses

## Overview
Perintah `iotop` digunakan untuk memantau penggunaan I/O disk secara real-time oleh proses yang berjalan di sistem Linux. Ini sangat berguna untuk mengidentifikasi proses mana yang menggunakan sumber daya disk secara berlebihan, sehingga Anda dapat melakukan tindakan yang diperlukan untuk mengoptimalkan kinerja sistem.

## Usage
Berikut adalah sintaks dasar dari perintah `iotop`:

```bash
iotop [options] [arguments]
```

## Common Options
- `-o` atau `--only`: Menampilkan hanya proses yang sedang melakukan I/O.
- `-b` atau `--batch`: Menjalankan `iotop` dalam mode batch, berguna untuk output ke file.
- `-n NUM`: Menentukan jumlah iterasi yang akan dilakukan sebelum keluar.
- `-d SEC`: Menentukan interval waktu (dalam detik) antara pembaruan tampilan.

## Common Examples
Berikut adalah beberapa contoh penggunaan `iotop`:

1. Menjalankan `iotop` untuk melihat semua proses yang menggunakan I/O:
   ```bash
   iotop
   ```

2. Menjalankan `iotop` hanya untuk menampilkan proses yang sedang melakukan I/O:
   ```bash
   iotop -o
   ```

3. Menjalankan `iotop` dalam mode batch dan menyimpan output ke file:
   ```bash
   iotop -b -n 10 > iotop_output.txt
   ```

4. Menjalankan `iotop` dengan interval pembaruan 2 detik:
   ```bash
   iotop -d 2
   ```

## Tips
- Gunakan opsi `-o` untuk fokus pada proses yang aktif melakukan I/O, sehingga lebih mudah untuk mengidentifikasi masalah.
- Pertimbangkan untuk menjalankan `iotop` dengan hak akses root untuk mendapatkan informasi yang lebih lengkap tentang semua proses.
- Jika Anda ingin memantau I/O dalam jangka waktu tertentu, gunakan opsi `-n` untuk mengatur jumlah iterasi yang diinginkan.