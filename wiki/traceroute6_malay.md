# [Linux] Bash traceroute6 Penggunaan: Menjejak laluan IPv6

## Overview
Perintah `traceroute6` digunakan untuk menjejak laluan yang dilalui oleh paket data melalui rangkaian IPv6. Ia membantu pengguna memahami bagaimana data bergerak dari satu titik ke titik lain dalam rangkaian dan mengenal pasti sebarang masalah yang mungkin berlaku.

## Usage
Sintaks asas untuk menggunakan `traceroute6` adalah seperti berikut:
```bash
traceroute6 [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk `traceroute6` beserta penjelasannya:
- `-m <max_ttl>`: Menetapkan nilai maksimum Time To Live (TTL) untuk paket.
- `-p <port>`: Menentukan port yang akan digunakan untuk sambungan.
- `-n`: Mengelakkan penyelesaian nama host, hanya menunjukkan alamat IP.
- `-w <timeout>`: Menetapkan masa tamat untuk menunggu balasan dari setiap hop.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `traceroute6`:

1. Menjejak laluan ke alamat IPv6 tertentu:
   ```bash
   traceroute6 google.com
   ```

2. Menetapkan nilai maksimum TTL kepada 30:
   ```bash
   traceroute6 -m 30 google.com
   ```

3. Menggunakan port tertentu, contohnya port 80:
   ```bash
   traceroute6 -p 80 google.com
   ```

4. Mengelakkan penyelesaian nama host:
   ```bash
   traceroute6 -n google.com
   ```

## Tips
- Gunakan pilihan `-n` jika anda ingin mempercepatkan proses traceroute, terutamanya dalam rangkaian yang besar.
- Sentiasa periksa sambungan rangkaian anda sebelum menggunakan `traceroute6` untuk memastikan hasil yang tepat.
- Jika anda menghadapi masalah, cuba gunakan pilihan `-w` untuk menyesuaikan masa tamat dan lihat jika itu membantu mendapatkan hasil yang lebih baik.