# [Linux] Bash dig Penggunaan: Mengambil maklumat DNS

## Overview
Perintah `dig` (Domain Information Groper) digunakan untuk mengambil maklumat DNS (Domain Name System) dari pelayan DNS. Ia membolehkan pengguna untuk melakukan pencarian DNS dan mendapatkan maklumat seperti alamat IP, rekod MX, dan banyak lagi.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `dig`:

```bash
dig [options] [arguments]
```

## Common Options
- `@server` : Menentukan pelayan DNS yang ingin digunakan untuk pencarian.
- `-t type` : Menentukan jenis rekod yang ingin dicari (contoh: A, MX, TXT).
- `+short` : Menunjukkan hasil dalam format ringkas.
- `+trace` : Mengikuti rantaian pencarian DNS dari akar hingga ke pelayan yang ditentukan.

## Common Examples
1. **Mencari alamat IP untuk domain:**
   ```bash
   dig example.com
   ```

2. **Mencari rekod MX untuk domain:**
   ```bash
   dig -t MX example.com
   ```

3. **Menggunakan pelayan DNS tertentu:**
   ```bash
   dig @8.8.8.8 example.com
   ```

4. **Mendapatkan hasil ringkas:**
   ```bash
   dig +short example.com
   ```

5. **Mengikuti rantaian pencarian DNS:**
   ```bash
   dig +trace example.com
   ```

## Tips
- Gunakan `+short` untuk mendapatkan hasil yang lebih mudah dibaca, terutama jika anda hanya memerlukan alamat IP.
- Jika anda sering menggunakan pelayan DNS tertentu, pertimbangkan untuk menetapkannya dalam fail konfigurasi resolv.conf.
- Untuk analisis yang lebih mendalam, gunakan pilihan `+stats` untuk mendapatkan maklumat tambahan tentang pencarian DNS yang dilakukan.