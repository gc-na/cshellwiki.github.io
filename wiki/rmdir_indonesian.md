# [Linux] Bash rmdir Penggunaan: Menghapus direktori kosong

## Overview
Perintah `rmdir` digunakan untuk menghapus direktori yang kosong. Jika direktori yang ingin dihapus berisi file atau subdirektori, perintah ini tidak akan berhasil dan akan memberikan pesan kesalahan.

## Usage
Berikut adalah sintaks dasar dari perintah `rmdir`:

```
rmdir [options] [arguments]
```

## Common Options
- `-p`: Menghapus direktori beserta direktori induknya jika direktori induk tersebut juga kosong.
- `--ignore-fail-on-non-empty`: Mengabaikan kesalahan jika direktori tidak kosong.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `rmdir`:

1. Menghapus direktori kosong:
   ```bash
   rmdir direktori_kosong
   ```

2. Menghapus beberapa direktori kosong sekaligus:
   ```bash
   rmdir direktori1 direktori2
   ```

3. Menghapus direktori beserta direktori induknya jika keduanya kosong:
   ```bash
   rmdir -p direktori_induk/direktori_kosong
   ```

4. Mengabaikan kesalahan jika direktori tidak kosong:
   ```bash
   rmdir --ignore-fail-on-non-empty direktori_tidak_kosong
   ```

## Tips
- Pastikan direktori yang ingin dihapus benar-benar kosong sebelum menggunakan `rmdir`.
- Gunakan opsi `-p` dengan hati-hati, karena ini dapat menghapus lebih dari satu direktori sekaligus.
- Untuk menghapus direktori yang tidak kosong, pertimbangkan untuk menggunakan perintah `rm -r` sebagai alternatif.