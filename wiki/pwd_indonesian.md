# [Sistem Operasi] C Shell (csh) pwd: Menampilkan direktori kerja saat ini

## Overview
Perintah `pwd` (print working directory) digunakan untuk menampilkan jalur direktori kerja saat ini di dalam terminal. Ini sangat berguna untuk mengetahui di mana Anda berada dalam struktur direktori.

## Usage
Sintaks dasar dari perintah `pwd` adalah sebagai berikut:

```
pwd [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan perintah `pwd`:

- `-L`: Menampilkan jalur direktori yang sebenarnya, mengikuti simbolik link.
- `-P`: Menampilkan jalur direktori fisik, tanpa mengikuti simbolik link.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `pwd`:

1. Menampilkan direktori kerja saat ini:
   ```csh
   pwd
   ```

2. Menampilkan jalur direktori secara fisik:
   ```csh
   pwd -P
   ```

3. Menampilkan jalur direktori dengan mengikuti simbolik link:
   ```csh
   pwd -L
   ```

## Tips
- Gunakan `pwd` secara berkala untuk memastikan Anda berada di direktori yang tepat sebelum menjalankan perintah lain.
- Kombinasikan `pwd` dengan perintah lain seperti `cd` untuk navigasi yang lebih efisien dalam terminal.
- Jika Anda bekerja dengan skrip, pertimbangkan untuk menyimpan output dari `pwd` ke dalam variabel untuk referensi di kemudian hari.