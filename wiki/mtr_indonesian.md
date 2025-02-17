# [Linux] Bash mtr Penggunaan: Mendiagnosis konektivitas jaringan

## Overview
Perintah `mtr` (My Traceroute) adalah alat yang menggabungkan fungsi dari `ping` dan `traceroute`. Ini digunakan untuk mendiagnosis konektivitas jaringan dengan memberikan informasi tentang jalur yang dilalui paket data ke tujuan tertentu serta waktu respons dari setiap hop.

## Usage
Sintaks dasar dari perintah `mtr` adalah sebagai berikut:

```bash
mtr [options] [arguments]
```

## Common Options
- `-r`: Menjalankan dalam mode laporan, hanya menampilkan hasil akhir.
- `-c <count>`: Menentukan jumlah ping yang akan dikirim.
- `-i <interval>`: Menentukan interval waktu antara pengiriman ping.
- `-p`: Menampilkan informasi port.
- `-w`: Menampilkan output dalam format yang lebih lebar.

## Common Examples
Berikut adalah beberapa contoh penggunaan `mtr`:

1. Menjalankan `mtr` ke sebuah alamat IP atau domain:
   ```bash
   mtr google.com
   ```

2. Menggunakan mode laporan untuk mendapatkan hasil akhir setelah beberapa ping:
   ```bash
   mtr -r -c 10 google.com
   ```

3. Menentukan interval waktu antara ping:
   ```bash
   mtr -i 2 google.com
   ```

4. Menampilkan informasi port:
   ```bash
   mtr -p google.com
   ```

5. Menjalankan `mtr` dengan output lebar:
   ```bash
   mtr -w google.com
   ```

## Tips
- Gunakan opsi `-r` untuk mendapatkan ringkasan cepat dari hasil pengujian.
- Jika Anda ingin memantau konektivitas secara berkelanjutan, jalankan `mtr` tanpa opsi tambahan.
- Perhatikan waktu respons dari setiap hop untuk mengidentifikasi titik masalah dalam jaringan.
- Kombinasikan `mtr` dengan opsi lain untuk mendapatkan informasi yang lebih spesifik sesuai kebutuhan Anda.