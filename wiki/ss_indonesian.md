# [Linux] Bash ss Penggunaan: Menampilkan soket jaringan

## Overview
Perintah `ss` adalah alat yang digunakan untuk menampilkan informasi tentang soket jaringan di sistem Linux. Ini memberikan rincian tentang koneksi TCP, UDP, dan soket lainnya, serta status dan statistik yang berkaitan dengan mereka. `ss` adalah pengganti yang lebih cepat dan lebih efisien untuk perintah `netstat`.

## Usage
Berikut adalah sintaks dasar dari perintah `ss`:

```bash
ss [options] [arguments]
```

## Common Options
- `-t`: Menampilkan soket TCP.
- `-u`: Menampilkan soket UDP.
- `-l`: Menampilkan soket yang sedang mendengarkan.
- `-p`: Menampilkan proses yang menggunakan soket.
- `-n`: Menampilkan alamat dan port dalam format numerik.
- `-s`: Menampilkan ringkasan statistik soket.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `ss`:

1. Menampilkan semua koneksi TCP:
   ```bash
   ss -t
   ```

2. Menampilkan semua soket UDP:
   ```bash
   ss -u
   ```

3. Menampilkan soket yang sedang mendengarkan:
   ```bash
   ss -l
   ```

4. Menampilkan semua soket dengan informasi proses:
   ```bash
   ss -p
   ```

5. Menampilkan semua soket dengan alamat dan port dalam format numerik:
   ```bash
   ss -n
   ```

6. Menampilkan ringkasan statistik soket:
   ```bash
   ss -s
   ```

## Tips
- Gunakan opsi `-n` untuk mempercepat output dengan menghindari resolusi nama host.
- Kombinasikan beberapa opsi untuk mendapatkan informasi yang lebih lengkap, misalnya `ss -tunlp` untuk melihat semua soket TCP dan UDP yang mendengarkan beserta prosesnya.
- Perintah `ss` dapat dijalankan dengan hak akses root untuk mendapatkan informasi lebih lengkap tentang semua soket yang ada di sistem.