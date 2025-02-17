# [Linux] Bash pvs Penggunaan: Menampilkan informasi tentang volume fisik

## Overview
Perintah `pvs` digunakan untuk menampilkan informasi tentang volume fisik dalam sistem manajemen volume logis (LVM) di Linux. Dengan menggunakan `pvs`, pengguna dapat melihat detail seperti ukuran, status, dan atribut dari volume fisik yang ada.

## Usage
Berikut adalah sintaks dasar dari perintah `pvs`:

```bash
pvs [options] [arguments]
```

## Common Options
- `-o, --options`: Menentukan kolom mana yang akan ditampilkan.
- `-f, --full`: Menampilkan informasi lengkap tentang volume fisik.
- `-a, --all`: Menampilkan semua volume fisik, termasuk yang tidak aktif.
- `-h, --help`: Menampilkan bantuan tentang penggunaan perintah.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `pvs`:

1. **Menampilkan semua volume fisik:**
   ```bash
   pvs
   ```

2. **Menampilkan informasi lengkap tentang volume fisik:**
   ```bash
   pvs -f
   ```

3. **Menampilkan volume fisik dengan kolom tertentu:**
   ```bash
   pvs -o +pv_size,pv_uuid
   ```

4. **Menampilkan semua volume fisik, termasuk yang tidak aktif:**
   ```bash
   pvs -a
   ```

## Tips
- Gunakan opsi `-o` untuk menyesuaikan informasi yang ingin Anda lihat, sehingga Anda hanya mendapatkan data yang relevan.
- Periksa status volume fisik secara berkala untuk memastikan tidak ada masalah dengan penyimpanan Anda.
- Kombinasikan `pvs` dengan perintah lain seperti `vgs` dan `lvs` untuk mendapatkan gambaran menyeluruh tentang sistem LVM Anda.