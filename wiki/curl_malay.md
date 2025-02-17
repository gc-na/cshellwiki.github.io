# [Linux] Bash curl Penggunaan: Mengambil dan menghantar data melalui URL

## Overview
Perintah `curl` adalah alat baris perintah yang digunakan untuk menghantar dan menerima data melalui URL. Ia menyokong pelbagai protokol seperti HTTP, HTTPS, FTP, dan banyak lagi. `curl` sering digunakan untuk menguji API, memuat turun fail, dan menghantar data ke pelayan.

## Usage
Sintaks asas untuk menggunakan `curl` adalah seperti berikut:

```bash
curl [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk `curl` beserta penjelasan ringkas:

- `-X`: Menentukan jenis permintaan HTTP (contoh: GET, POST).
- `-d`: Menghantar data dalam permintaan POST.
- `-H`: Menambah header khusus pada permintaan.
- `-o`: Menyimpan output ke dalam fail.
- `-I`: Mengambil hanya header respons.

## Common Examples
Berikut adalah beberapa contoh praktikal menggunakan `curl`:

1. **Mengambil halaman web:**
   ```bash
   curl https://www.example.com
   ```

2. **Menghantar permintaan POST dengan data:**
   ```bash
   curl -X POST -d "name=John&age=30" https://www.example.com/api
   ```

3. **Mengambil hanya header respons:**
   ```bash
   curl -I https://www.example.com
   ```

4. **Menyimpan output ke dalam fail:**
   ```bash
   curl -o myfile.html https://www.example.com
   ```

5. **Menambah header khusus:**
   ```bash
   curl -H "Authorization: Bearer token" https://www.example.com/api
   ```

## Tips
- Sentiasa semak dokumentasi rasmi `curl` untuk pilihan dan parameter tambahan.
- Gunakan `-v` untuk mengaktifkan mod verbose, yang memberikan maklumat lebih terperinci tentang permintaan dan respons.
- Untuk menguji API, pertimbangkan untuk menggunakan alat seperti Postman, tetapi `curl` adalah pilihan yang hebat untuk automasi skrip.
- Simpan skrip `curl` yang sering digunakan dalam fail `.sh` untuk kemudahan akses di masa hadapan.