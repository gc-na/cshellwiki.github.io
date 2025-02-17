# [Linux] Bash uptime Penggunaan: Menampilkan waktu aktif sistem

## Overview
Perintah `uptime` digunakan untuk menampilkan berapa lama sistem telah berjalan sejak terakhir kali dinyalakan. Selain itu, perintah ini juga memberikan informasi tentang jumlah pengguna yang sedang aktif dan beban rata-rata sistem dalam periode waktu tertentu.

## Usage
Berikut adalah sintaks dasar dari perintah `uptime`:

```
uptime [options]
```

## Common Options
- `-p` : Menampilkan waktu aktif dalam format yang lebih mudah dibaca.
- `-s` : Menampilkan waktu sistem terakhir dinyalakan.
- `-h` : Menampilkan bantuan untuk perintah `uptime`.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `uptime`:

1. Menampilkan waktu aktif sistem saat ini:
   ```bash
   uptime
   ```

2. Menampilkan waktu aktif dalam format yang lebih mudah dibaca:
   ```bash
   uptime -p
   ```

3. Menampilkan waktu terakhir sistem dinyalakan:
   ```bash
   uptime -s
   ```

4. Menampilkan informasi uptime dengan bantuan:
   ```bash
   uptime -h
   ```

## Tips
- Gunakan opsi `-p` untuk mendapatkan informasi yang lebih ringkas dan mudah dipahami tentang waktu aktif sistem.
- Periksa beban rata-rata yang ditampilkan oleh `uptime` untuk memantau kinerja sistem secara keseluruhan.
- Kombinasikan `uptime` dengan perintah lain seperti `top` atau `htop` untuk analisis lebih mendalam tentang penggunaan sumber daya sistem.