# [Linux] Bash unxz Penggunaan: Menghapus kompresi file .xz

## Overview
Perintah `unxz` digunakan untuk menghapus kompresi dari file yang dikompresi menggunakan algoritma XZ. File yang dikompresi dengan ekstensi `.xz` dapat dikembalikan ke bentuk aslinya dengan menggunakan perintah ini.

## Usage
Berikut adalah sintaks dasar dari perintah `unxz`:

```
unxz [options] [arguments]
```

## Common Options
- `-k`, `--keep`: Menyimpan file asli setelah dekompresi.
- `-f`, `--force`: Memaksa penggantian file yang sudah ada tanpa meminta konfirmasi.
- `-v`, `--verbose`: Menampilkan informasi lebih rinci selama proses dekompresi.

## Common Examples
Berikut adalah beberapa contoh penggunaan `unxz`:

1. **Menghapus kompresi dari file .xz**:
   ```bash
   unxz file.txt.xz
   ```

2. **Menghapus kompresi dan menyimpan file asli**:
   ```bash
   unxz -k file.txt.xz
   ```

3. **Memaksa penggantian file yang sudah ada**:
   ```bash
   unxz -f file.txt.xz
   ```

4. **Menampilkan informasi selama proses dekompresi**:
   ```bash
   unxz -v file.txt.xz
   ```

## Tips
- Selalu periksa apakah Anda memiliki cadangan file asli sebelum menggunakan opsi `-f` untuk menghindari kehilangan data.
- Gunakan opsi `-k` jika Anda ingin menjaga file kompresi setelah dekompresi, sehingga Anda dapat menggunakannya lagi di masa mendatang.
- Jika Anda bekerja dengan banyak file, pertimbangkan untuk menggunakan wildcard, seperti `*.xz`, untuk mendekompresi beberapa file sekaligus.