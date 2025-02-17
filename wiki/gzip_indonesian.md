# [Linux] Bash gzip Penggunaan: Mengompresi file

## Overview
Perintah `gzip` adalah alat yang digunakan untuk mengompresi file di sistem operasi Unix dan Linux. Gzip mengurangi ukuran file dengan menggunakan algoritma kompresi yang efisien, sehingga menghemat ruang penyimpanan.

## Usage
Sintaks dasar dari perintah `gzip` adalah sebagai berikut:

```bash
gzip [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan perintah `gzip`:

- `-d` atau `--decompress`: Mengompresi file yang sudah terkompresi.
- `-k` atau `--keep`: Menyimpan file asli setelah kompresi.
- `-v` atau `--verbose`: Menampilkan informasi lebih detail selama proses kompresi.
- `-r` atau `--recursive`: Mengompresi file dalam direktori secara rekursif.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `gzip`:

1. Mengompresi file:
   ```bash
   gzip file.txt
   ```

2. Mengompresi file dan menyimpan file asli:
   ```bash
   gzip -k file.txt
   ```

3. Mengompresi semua file dalam direktori:
   ```bash
   gzip *.txt
   ```

4. Menggunakan opsi verbose untuk melihat proses kompresi:
   ```bash
   gzip -v file.txt
   ```

5. Meng-dekompresi file:
   ```bash
   gzip -d file.txt.gz
   ```

## Tips
- Selalu gunakan opsi `-k` jika Anda ingin menjaga file asli setelah kompresi.
- Untuk mengompresi banyak file sekaligus, gunakan wildcard (`*`) untuk memilih file yang ingin dikompresi.
- Periksa ukuran file setelah kompresi untuk memastikan penghematan ruang yang diinginkan.