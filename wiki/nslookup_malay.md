# [Linux] Bash nslookup Penggunaan: Memeriksa alamat IP dan nama domain

## Overview
Perintah `nslookup` digunakan untuk mencari maklumat mengenai sistem nama domain (DNS). Ia membolehkan pengguna untuk mendapatkan alamat IP bagi nama domain tertentu atau sebaliknya, serta maklumat lain yang berkaitan dengan DNS.

## Usage
Sintaks asas untuk menggunakan `nslookup` adalah seperti berikut:

```
nslookup [options] [arguments]
```

## Common Options
- `-type=TYPE` : Menentukan jenis rekod DNS yang ingin dicari (contoh: A, AAAA, MX).
- `-debug` : Mengaktifkan mod debug untuk mendapatkan maklumat tambahan tentang proses pencarian.
- `-timeout=SECONDS` : Menentukan masa tunggu untuk permintaan DNS dalam detik.

## Common Examples
Berikut adalah beberapa contoh penggunaan `nslookup`:

1. **Mendapatkan alamat IP bagi nama domain:**
   ```bash
   nslookup example.com
   ```

2. **Mencari jenis rekod tertentu (contoh: MX):**
   ```bash
   nslookup -type=MX example.com
   ```

3. **Menggunakan pelayan DNS tertentu:**
   ```bash
   nslookup example.com 8.8.8.8
   ```

4. **Mengaktifkan mod debug:**
   ```bash
   nslookup -debug example.com
   ```

## Tips
- Sentiasa gunakan pelayan DNS yang dipercayai untuk mendapatkan maklumat yang tepat.
- Gunakan pilihan `-type` untuk mendapatkan maklumat spesifik yang anda perlukan.
- Jika anda sering melakukan pencarian DNS, pertimbangkan untuk membuat skrip untuk mempercepatkan proses tersebut.