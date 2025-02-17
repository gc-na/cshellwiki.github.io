# [Linux] Bash traceroute Penggunaan: Menjejak laluan rangkaian

## Overview
Perintah `traceroute` digunakan untuk menjejak laluan yang diambil oleh paket data dari komputer anda ke alamat IP atau nama domain tertentu. Ia membantu dalam mendiagnosis masalah rangkaian dengan menunjukkan setiap hop (peranti penghala) yang dilalui oleh data.

## Usage
Sintaks asas untuk menggunakan perintah `traceroute` adalah seperti berikut:

```bash
traceroute [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan umum yang boleh digunakan dengan `traceroute`:

- `-m <max_ttl>`: Menetapkan nilai maksimum Time To Live (TTL) untuk paket.
- `-n`: Mengelakkan penukaran alamat IP kepada nama host.
- `-p <port>`: Menetapkan port yang akan digunakan untuk sambungan.
- `-w <timeout>`: Menetapkan masa tunggu untuk setiap jawapan.

## Common Examples
Berikut adalah beberapa contoh penggunaan `traceroute`:

1. Menjejak laluan ke alamat IP:
   ```bash
   traceroute 8.8.8.8
   ```

2. Menjejak laluan ke nama domain:
   ```bash
   traceroute www.google.com
   ```

3. Menggunakan pilihan `-n` untuk mengelakkan penukaran nama:
   ```bash
   traceroute -n 8.8.8.8
   ```

4. Menetapkan nilai maksimum TTL:
   ```bash
   traceroute -m 15 www.example.com
   ```

5. Menggunakan port tertentu:
   ```bash
   traceroute -p 80 www.example.com
   ```

## Tips
- Gunakan pilihan `-n` jika anda ingin mendapatkan hasil lebih cepat tanpa menunggu penukaran nama.
- Perhatikan bahawa beberapa rangkaian mungkin tidak membenarkan `traceroute` berfungsi dengan baik, jadi hasil mungkin berbeza.
- Jika anda mengalami masalah sambungan, periksa setiap hop untuk mengenal pasti di mana masalah mungkin berlaku.