# [Linux] Bash rm Penggunaan: Menghapus fail dan direktori

## Overview
Perintah `rm` dalam Bash digunakan untuk menghapus fail dan direktori dari sistem fail. Ia adalah alat yang kuat dan harus digunakan dengan berhati-hati kerana ia tidak memindahkan fail ke tong sampah; sebaliknya, ia menghapus fail secara kekal.

## Usage
Sintaks asas untuk perintah `rm` adalah seperti berikut:

```bash
rm [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa yang digunakan dengan perintah `rm`:

- `-f`: Memaksa penghapusan tanpa meminta pengesahan.
- `-i`: Meminta pengesahan sebelum menghapus setiap fail.
- `-r`: Menghapus direktori dan semua fail di dalamnya secara rekursif.
- `-v`: Menunjukkan fail yang sedang dihapuskan.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan perintah `rm`:

1. Menghapus fail tunggal:
   ```bash
   rm fail.txt
   ```

2. Menghapus fail dengan pengesahan:
   ```bash
   rm -i fail.txt
   ```

3. Menghapus direktori dan semua isinya:
   ```bash
   rm -r direktori/
   ```

4. Menghapus fail tanpa meminta pengesahan:
   ```bash
   rm -f fail.txt
   ```

5. Menghapus semua fail dengan sambungan tertentu:
   ```bash
   rm *.log
   ```

## Tips
- Sentiasa gunakan pilihan `-i` jika anda tidak pasti tentang fail yang akan dihapuskan.
- Sebelum menggunakan `rm -r`, pastikan anda berada dalam direktori yang betul untuk mengelakkan penghapusan data yang tidak diingini.
- Pertimbangkan untuk menggunakan perintah `mv` untuk memindahkan fail ke direktori lain sebelum menghapusnya, sebagai langkah berjaga-jaga.