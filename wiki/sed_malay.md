# [Linux] Bash sed Penggunaan: Mengedit teks dalam aliran

## Overview
Perintah `sed` (stream editor) digunakan untuk mengedit teks dalam aliran. Ia membolehkan pengguna untuk melakukan pelbagai operasi seperti mencari, mengganti, dan memformat teks secara langsung dalam fail atau input dari aliran.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `sed`:

```bash
sed [options] [arguments]
```

## Common Options
- `-e`: Menentukan arahan yang akan dilaksanakan.
- `-i`: Mengedit fail secara langsung (in-place).
- `-n`: Menonaktifkan output secara lalai; hanya output yang ditentukan akan dipaparkan.
- `s`: Melakukan pencarian dan penggantian.

## Common Examples

1. **Menggantikan teks dalam fail**:
   Menggantikan semua kemunculan "lama" dengan "baru" dalam fail `contoh.txt`.
   ```bash
   sed -i 's/lama/baru/g' contoh.txt
   ```

2. **Menampilkan baris tertentu**:
   Menampilkan baris ke-2 hingga ke-4 dari fail `contoh.txt`.
   ```bash
   sed -n '2,4p' contoh.txt
   ```

3. **Menghapus baris yang mengandungi teks tertentu**:
   Menghapus semua baris yang mengandungi "hapus" dari fail `contoh.txt`.
   ```bash
   sed -i '/hapus/d' contoh.txt
   ```

4. **Menggantikan teks dalam input dari arahan lain**:
   Menggantikan "lama" dengan "baru" dalam output arahan `echo`.
   ```bash
   echo "Ini adalah teks lama" | sed 's/lama/baru/'
   ```

## Tips
- Selalu buat salinan fail sebelum menggunakan `-i` untuk mengedit secara langsung, bagi mengelakkan kehilangan data.
- Gunakan `-n` bersama dengan arahan `p` untuk mengawal output dan hanya memaparkan hasil yang diperlukan.
- Pelajari penggunaan ekspresi reguler untuk meningkatkan keupayaan pencarian dan penggantian dalam `sed`.