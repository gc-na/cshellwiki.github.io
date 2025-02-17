# [Linux] Bash htop Penggunaan: Memantau penggunaan sumber daya sistem

## Overview
Perintah `htop` adalah alat interaktif yang digunakan untuk memantau penggunaan sumber daya sistem secara real-time. Ini memberikan tampilan yang lebih informatif dan mudah dibaca dibandingkan dengan perintah `top`, memungkinkan pengguna untuk melihat proses yang sedang berjalan, penggunaan CPU, memori, dan swap dengan cara yang lebih intuitif.

## Usage
Sintaks dasar untuk menjalankan perintah htop adalah sebagai berikut:

```bash
htop [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan htop:

- `-d <delay>`: Mengatur interval pembaruan dalam detik.
- `-u <user>`: Menampilkan hanya proses yang dimiliki oleh pengguna tertentu.
- `-p <pid>`: Menampilkan hanya proses dengan ID proses tertentu.
- `--help`: Menampilkan informasi bantuan tentang penggunaan htop.

## Common Examples
Berikut adalah beberapa contoh penggunaan htop:

1. Menjalankan htop tanpa opsi:
   ```bash
   htop
   ```

2. Menjalankan htop dengan interval pembaruan 2 detik:
   ```bash
   htop -d 2
   ```

3. Menampilkan proses hanya untuk pengguna tertentu:
   ```bash
   htop -u username
   ```

4. Menampilkan proses dengan ID tertentu:
   ```bash
   htop -p 1234
   ```

## Tips
- Gunakan tombol `F2` untuk mengakses menu pengaturan dan menyesuaikan tampilan htop sesuai kebutuhan Anda.
- Anda dapat menggunakan tombol panah untuk menavigasi antar proses dan `F9` untuk menghentikan proses yang dipilih.
- Htop juga memungkinkan Anda untuk memfilter proses dengan menekan `F3` dan memasukkan nama proses yang ingin dicari.