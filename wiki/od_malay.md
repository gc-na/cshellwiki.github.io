# [Linux] Bash od Penggunaan: Menampilkan kandungan fail dalam pelbagai format

## Overview
Perintah `od` (octal dump) digunakan untuk menampilkan kandungan fail dalam pelbagai format, termasuk octal, heksadesimal, dan ASCII. Ia berguna untuk menganalisis fail binari dan memahami struktur data.

## Usage
Sintaks asas untuk menggunakan perintah `od` adalah seperti berikut:

```
od [options] [arguments]
```

## Common Options
- `-A, --address-radix=RADIX` : Menentukan format alamat (o untuk octal, x untuk heksadesimal, d untuk decimal).
- `-t, --output-format=TYPE` : Menentukan format output (contoh: a untuk ASCII, o untuk octal, x untuk heksadesimal).
- `-N, --read-bytes=N` : Membaca hanya N bait dari fail.
- `-v, --output-duplicates` : Menampilkan semua output, termasuk duplikasi.

## Common Examples
1. Menampilkan kandungan fail dalam format heksadesimal:
   ```bash
   od -x fail.bin
   ```

2. Menampilkan kandungan fail dalam format ASCII:
   ```bash
   od -c fail.txt
   ```

3. Menampilkan 16 bait pertama dalam format octal:
   ```bash
   od -N 16 -o fail.bin
   ```

4. Menampilkan alamat dalam format heksadesimal dan kandungan dalam format ASCII:
   ```bash
   od -A x -t x1 -c fail.bin
   ```

## Tips
- Gunakan `-v` untuk memastikan semua data ditunjukkan, terutamanya jika anda bekerja dengan fail yang mempunyai banyak nilai yang sama.
- Eksperimen dengan pelbagai format output untuk mendapatkan pandangan yang lebih baik tentang data dalam fail.
- Ingat untuk menggunakan `man od` untuk mendapatkan maklumat lanjut tentang pilihan dan penggunaan perintah ini.