# [Linux] Bash traceroute6 Penggunaan: Menelusuri jalur IPv6

## Overview
Perintah `traceroute6` digunakan untuk melacak jalur yang dilalui paket data dalam jaringan berbasis IPv6. Dengan menggunakan perintah ini, pengguna dapat melihat setiap hop atau titik yang dilalui oleh data dari sumber ke tujuan, yang sangat berguna untuk mendiagnosis masalah jaringan.

## Usage
Berikut adalah sintaks dasar dari perintah `traceroute6`:

```bash
traceroute6 [options] [arguments]
```

## Common Options
- `-m <max_ttl>`: Menentukan nilai maksimum Time To Live (TTL) untuk paket yang dikirim.
- `-p <port>`: Menentukan port yang akan digunakan untuk pengujian.
- `-n`: Menghindari resolusi nama host, hanya menampilkan alamat IP.
- `-w <timeout>`: Menentukan waktu tunggu untuk setiap respons.

## Common Examples
Berikut adalah beberapa contoh penggunaan `traceroute6`:

1. Menelusuri jalur ke alamat IPv6 tertentu:
   ```bash
   traceroute6 2001:db8::1
   ```

2. Menelusuri jalur dengan batas TTL maksimum 30:
   ```bash
   traceroute6 -m 30 2001:db8::1
   ```

3. Menelusuri jalur tanpa resolusi nama host:
   ```bash
   traceroute6 -n 2001:db8::1
   ```

4. Menelusuri jalur dengan port tertentu (misalnya port 80):
   ```bash
   traceroute6 -p 80 2001:db8::1
   ```

## Tips
- Gunakan opsi `-n` untuk mempercepat proses jika Anda tidak memerlukan nama host.
- Periksa pengaturan firewall Anda jika Anda tidak mendapatkan respons dari beberapa hop.
- Cobalah menggunakan `traceroute6` dari berbagai lokasi untuk mendapatkan gambaran yang lebih baik tentang jalur jaringan.