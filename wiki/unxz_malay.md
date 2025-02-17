# [Linux] Bash unxz Penggunaan: Mengeluarkan fail .xz

## Overview
Perintah `unxz` digunakan untuk mengekstrak fail yang telah dimampatkan menggunakan algoritma XZ. Ia adalah alat yang berguna untuk mengembalikan fail kepada bentuk asalnya selepas pemampatan.

## Usage
Sintaks asas bagi perintah `unxz` adalah seperti berikut:

```
unxz [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan umum untuk `unxz` beserta penjelasannya:

- `-k` : Menyimpan fail asal yang dimampatkan selepas proses pengeluaran.
- `-v` : Menunjukkan maklumat terperinci semasa proses pengeluaran.
- `-f` : Memaksa pengeluaran walaupun fail dengan nama yang sama sudah wujud.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `unxz`:

1. **Mengeluarkan fail .xz**:
   ```bash
   unxz fail.txt.xz
   ```

2. **Mengeluarkan fail dan menyimpan fail asal**:
   ```bash
   unxz -k fail.txt.xz
   ```

3. **Mengeluarkan fail dengan maklumat terperinci**:
   ```bash
   unxz -v fail.txt.xz
   ```

4. **Memaksa pengeluaran walaupun fail dengan nama yang sama wujud**:
   ```bash
   unxz -f fail.txt.xz
   ```

## Tips
- Sentiasa semak ruang simpanan sebelum mengekstrak fail besar untuk mengelakkan masalah ruang.
- Gunakan pilihan `-k` jika anda ingin menyimpan fail asal untuk rujukan atau pemulihan.
- Untuk mengelakkan kehilangan data, pastikan anda mempunyai salinan fail penting sebelum menggunakan pilihan `-f`.