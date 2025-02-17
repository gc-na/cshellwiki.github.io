# [Linux] Bash basename Penggunaan: Mengambil nama file dari path

## Overview
Perintah `basename` digunakan untuk mengambil nama file dari sebuah path lengkap. Ini sangat berguna ketika Anda hanya ingin mendapatkan nama file tanpa direktori yang menyertainya.

## Usage
Berikut adalah sintaks dasar dari perintah `basename`:

```bash
basename [options] [arguments]
```

## Common Options
- `-a`: Mengambil semua nama file yang diberikan sebagai argumen.
- `-s`: Menghapus suffix tertentu dari nama file.
- `--help`: Menampilkan informasi bantuan tentang penggunaan `basename`.

## Common Examples

1. **Mengambil nama file dari path lengkap:**
   ```bash
   basename /home/user/documents/file.txt
   ```
   Output:
   ```
   file.txt
   ```

2. **Menghapus suffix dari nama file:**
   ```bash
   basename /home/user/documents/file.txt .txt
   ```
   Output:
   ```
   file
   ```

3. **Mengambil nama file dari beberapa path:**
   ```bash
   basename -a /home/user/documents/file1.txt /home/user/documents/file2.txt
   ```
   Output:
   ```
   file1.txt
   file2.txt
   ```

## Tips
- Gunakan opsi `-s` untuk menghapus ekstensi file yang tidak diinginkan saat mengambil nama file.
- Jika Anda bekerja dengan beberapa file, pertimbangkan untuk menggunakan opsi `-a` agar lebih efisien.
- Perintah `basename` sering digunakan dalam skrip untuk memproses nama file secara otomatis.