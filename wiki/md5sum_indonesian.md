# [Linux] Bash md5sum Penggunaan: Menghitung checksum MD5

## Overview
Perintah `md5sum` digunakan untuk menghitung dan memverifikasi checksum MD5 dari file. Checksum ini sering digunakan untuk memastikan integritas data, sehingga Anda dapat memeriksa apakah file telah berubah atau rusak.

## Usage
Sintaks dasar dari perintah `md5sum` adalah sebagai berikut:

```bash
md5sum [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan `md5sum`:

- `-b`: Menghitung checksum untuk file biner.
- `-c`: Memeriksa checksum dari file yang telah dihitung sebelumnya.
- `-t`: Menghitung checksum dari input teks.
- `--help`: Menampilkan bantuan penggunaan perintah.

## Common Examples

1. **Menghitung checksum MD5 dari sebuah file:**

   ```bash
   md5sum namafile.txt
   ```

2. **Menyimpan checksum ke dalam file:**

   ```bash
   md5sum namafile.txt > checksum.md5
   ```

3. **Memeriksa checksum dari file yang telah dihitung sebelumnya:**

   ```bash
   md5sum -c checksum.md5
   ```

4. **Menghitung checksum untuk file biner:**

   ```bash
   md5sum -b namafile.bin
   ```

## Tips
- Selalu simpan checksum yang dihitung dalam file terpisah untuk memudahkan verifikasi di masa depan.
- Gunakan opsi `-c` untuk memeriksa beberapa file sekaligus dengan satu perintah.
- Pastikan untuk menggunakan `md5sum` pada file yang tidak sedang diubah untuk mendapatkan hasil yang akurat.