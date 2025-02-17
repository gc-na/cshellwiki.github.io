# [Linux] Bash uname Penggunaan: Menunjukkan maklumat sistem

## Overview
Perintah `uname` digunakan untuk menampilkan maklumat mengenai sistem operasi yang sedang digunakan. Ia memberikan informasi seperti nama sistem, versi kernel, dan jenis mesin.

## Usage
Sintaks asas untuk menggunakan perintah `uname` adalah seperti berikut:

```
uname [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan umum untuk perintah `uname` beserta penjelasannya:

- `-a`: Menampilkan semua maklumat yang tersedia.
- `-s`: Menampilkan nama sistem.
- `-n`: Menampilkan nama nod (hostname).
- `-r`: Menampilkan versi kernel.
- `-v`: Menampilkan maklumat versi tambahan.
- `-m`: Menampilkan jenis mesin.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan perintah `uname`:

1. Menampilkan semua maklumat sistem:
   ```bash
   uname -a
   ```

2. Menampilkan nama sistem:
   ```bash
   uname -s
   ```

3. Menampilkan versi kernel:
   ```bash
   uname -r
   ```

4. Menampilkan jenis mesin:
   ```bash
   uname -m
   ```

## Tips
- Gunakan `uname -a` untuk mendapatkan gambaran menyeluruh tentang sistem anda dalam satu perintah.
- Perintah ini berguna untuk skrip automasi yang memerlukan maklumat sistem.
- Pastikan anda menjalankan perintah ini dalam terminal untuk mendapatkan hasil yang tepat.