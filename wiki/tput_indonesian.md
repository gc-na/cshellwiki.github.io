# [Linux] Bash tput Penggunaan: Mengatur tampilan terminal

## Overview
Perintah `tput` digunakan untuk mengatur tampilan terminal dengan mengontrol atribut seperti warna, posisi kursor, dan format teks. Ini memungkinkan pengguna untuk meningkatkan pengalaman pengguna di terminal dengan memberikan umpan balik visual yang lebih baik.

## Usage
Sintaks dasar dari perintah `tput` adalah sebagai berikut:

```
tput [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan `tput`:

- `setaf [n]`: Mengatur warna teks ke warna yang ditentukan oleh angka `n`.
- `setab [n]`: Mengatur warna latar belakang ke warna yang ditentukan oleh angka `n`.
- `bold`: Mengaktifkan teks tebal.
- `clear`: Menghapus layar terminal.
- `cup [x] [y]`: Memindahkan kursor ke posisi yang ditentukan oleh koordinat `x` dan `y`.

## Common Examples
Berikut adalah beberapa contoh praktis penggunaan `tput`:

1. Mengatur warna teks menjadi merah:
   ```bash
   tput setaf 1
   echo "Ini adalah teks merah"
   ```

2. Mengatur warna latar belakang menjadi biru dan teks menjadi putih:
   ```bash
   tput setab 4
   tput setaf 7
   echo "Latar belakang biru, teks putih"
   ```

3. Menghapus layar terminal:
   ```bash
   tput clear
   ```

4. Memindahkan kursor ke baris ke-5 dan kolom ke-10:
   ```bash
   tput cup 5 10
   echo "Kursor berada di baris 5 kolom 10"
   ```

5. Mengaktifkan teks tebal:
   ```bash
   tput bold
   echo "Ini adalah teks tebal"
   ```

## Tips
- Selalu gunakan `tput reset` di akhir skrip untuk mengembalikan pengaturan terminal ke keadaan semula.
- Cobalah berbagai kombinasi warna untuk menemukan skema yang paling nyaman untuk mata Anda.
- Gunakan `man tput` untuk melihat dokumentasi lengkap dan opsi lainnya yang tersedia.