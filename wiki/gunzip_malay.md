# [Linux] Bash gunzip: Mengeluarkan fail yang dimampatkan

## Overview
Perintah `gunzip` digunakan untuk mengeluarkan fail yang telah dimampatkan menggunakan algoritma gzip. Ia membolehkan pengguna untuk mengembalikan fail kepada bentuk asalnya, menjadikannya berguna untuk pengurusan fail dan pemindahan data.

## Usage
Sintaks asas untuk menggunakan `gunzip` adalah seperti berikut:

```
gunzip [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk perintah `gunzip`:

- `-c`: Mengeluarkan fail ke output standard (stdout) tanpa menghapus fail asal.
- `-f`: Memaksa pengeluaran walaupun fail yang sama sudah ada.
- `-k`: Menyimpan fail asal selepas pengeluaran.
- `-r`: Mengeluarkan semua fail dalam direktori secara rekursif.

## Common Examples
Berikut adalah beberapa contoh penggunaan `gunzip`:

1. Mengeluarkan fail gzip:
   ```bash
   gunzip fail.gz
   ```

2. Mengeluarkan fail gzip dan menyimpan fail asal:
   ```bash
   gunzip -k fail.gz
   ```

3. Mengeluarkan fail gzip ke output standard:
   ```bash
   gunzip -c fail.gz > fail.txt
   ```

4. Mengeluarkan semua fail gzip dalam direktori:
   ```bash
   gunzip -r direktori/
   ```

## Tips
- Sentiasa semak ruang penyimpanan sebelum menggunakan `gunzip`, kerana fail yang dikeluarkan mungkin memerlukan lebih banyak ruang.
- Gunakan pilihan `-k` jika anda ingin mengekalkan fail asal untuk rujukan atau pemulihan.
- Jika anda bekerja dengan banyak fail, pertimbangkan untuk menggunakan pilihan `-r` untuk mengeluarkan semua fail dalam satu arahan.