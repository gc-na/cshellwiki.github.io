# [Linux] Bash bzip2 Penggunaan: Memampatkan dan menyahmampatkan fail

## Overview
Perintah `bzip2` digunakan untuk memampatkan dan menyahmampatkan fail menggunakan algoritma pemampatan bzip2. Ia sangat berkesan dalam mengurangkan saiz fail, menjadikannya berguna untuk penyimpanan dan pemindahan data.

## Usage
Sintaks asas untuk menggunakan `bzip2` adalah seperti berikut:

```bash
bzip2 [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa yang boleh digunakan dengan `bzip2`:

- `-d` atau `--decompress`: Menyahmampatkan fail yang telah dimampatkan.
- `-k` atau `--keep`: Menyimpan fail asal selepas pemampatan.
- `-f` atau `--force`: Memaksa pemampatan walaupun fail dengan nama yang sama sudah wujud.
- `-v` atau `--verbose`: Menunjukkan maklumat terperinci semasa pemampatan atau penyahmampatan.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `bzip2`:

1. **Memampatkan fail**:
   ```bash
   bzip2 fail.txt
   ```
   Ini akan menghasilkan fail `fail.txt.bz2` dan menghapuskan `fail.txt` asal.

2. **Menyahmampatkan fail**:
   ```bash
   bzip2 -d fail.txt.bz2
   ```
   Ini akan menyahmampatkan `fail.txt.bz2` dan menghasilkan semula `fail.txt`.

3. **Menyimpan fail asal semasa memampatkan**:
   ```bash
   bzip2 -k fail.txt
   ```
   Ini akan menghasilkan `fail.txt.bz2` tetapi mengekalkan `fail.txt` asal.

4. **Memaksa pemampatan**:
   ```bash
   bzip2 -f fail.txt
   ```
   Jika `fail.txt.bz2` sudah wujud, ia akan ditimpa.

5. **Menunjukkan maklumat terperinci**:
   ```bash
   bzip2 -v fail.txt
   ```
   Ini akan menunjukkan proses pemampatan dengan maklumat tambahan.

## Tips
- Sentiasa buat salinan fail asal sebelum memampatkan jika anda tidak mahu kehilangan data.
- Gunakan pilihan `-k` jika anda ingin mengekalkan fail asal semasa memampatkan.
- Untuk pemampatan yang lebih baik, pertimbangkan untuk menggunakan `bzip2` bersama dengan `tar` untuk mengarkibkan beberapa fail sekaligus.