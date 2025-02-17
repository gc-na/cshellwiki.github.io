# [Linux] Bash wget Penggunaan: Mengunduh file dari internet

## Overview
Perintah `wget` adalah alat baris perintah yang digunakan untuk mengunduh file dari internet. Ia mendukung berbagai protokol seperti HTTP, HTTPS, dan FTP, serta dapat digunakan untuk mengunduh file secara langsung atau mengunduh seluruh situs web.

## Usage
Berikut adalah sintaks dasar dari perintah `wget`:

```
wget [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang sering digunakan dengan `wget`:

- `-O [file]`: Menyimpan file yang diunduh dengan nama yang ditentukan.
- `-c`: Melanjutkan unduhan yang terputus.
- `-r`: Mengunduh secara rekursif, cocok untuk mengunduh seluruh situs web.
- `-p`: Mengunduh semua elemen yang diperlukan untuk menampilkan halaman web secara lengkap.
- `--limit-rate=[rate]`: Membatasi kecepatan unduhan.

## Common Examples
Berikut adalah beberapa contoh praktis penggunaan `wget`:

1. **Mengunduh file tunggal:**
   ```bash
   wget https://example.com/file.zip
   ```

2. **Mengunduh file dengan nama yang berbeda:**
   ```bash
   wget -O myfile.zip https://example.com/file.zip
   ```

3. **Melanjutkan unduhan yang terputus:**
   ```bash
   wget -c https://example.com/largefile.zip
   ```

4. **Mengunduh seluruh situs web:**
   ```bash
   wget -r https://example.com
   ```

5. **Mengunduh halaman web beserta semua elemen yang diperlukan:**
   ```bash
   wget -p https://example.com/page.html
   ```

## Tips
- Selalu periksa izin dan kebijakan penggunaan situs web sebelum mengunduh konten secara besar-besaran.
- Gunakan opsi `--limit-rate` untuk menghindari membebani server dengan unduhan yang terlalu cepat.
- Pertimbangkan untuk menggunakan opsi `-N` untuk hanya mengunduh file yang lebih baru daripada yang sudah ada di sistem Anda.