# [Linux] Bash hexdump Penggunaan: Menampilkan data dalam format heksadesimal

## Overview
Perintah `hexdump` digunakan untuk menampilkan konten file dalam format heksadesimal. Ini sangat berguna untuk menganalisis file biner dan melihat representasi byte dari data.

## Usage
Berikut adalah sintaks dasar dari perintah `hexdump`:

```bash
hexdump [options] [arguments]
```

## Common Options
- `-C`: Menampilkan output dalam format heksadesimal dan ASCII.
- `-n <number>`: Menentukan jumlah byte yang akan ditampilkan.
- `-v`: Menampilkan semua byte, termasuk byte yang berulang.
- `-e <format>`: Menentukan format output yang diinginkan.

## Common Examples
Berikut adalah beberapa contoh penggunaan `hexdump`:

1. Menampilkan isi file dalam format heksadesimal:
   ```bash
   hexdump file.bin
   ```

2. Menampilkan 16 byte pertama dari file:
   ```bash
   hexdump -n 16 file.bin
   ```

3. Menampilkan output dalam format heksadesimal dan ASCII:
   ```bash
   hexdump -C file.bin
   ```

4. Menggunakan opsi format untuk menampilkan data dengan cara tertentu:
   ```bash
   hexdump -e '16/1 "%02x " "\n"' file.bin
   ```

## Tips
- Gunakan opsi `-C` untuk mendapatkan tampilan yang lebih mudah dibaca, terutama saat menganalisis file biner.
- Pertimbangkan untuk menggunakan opsi `-n` untuk membatasi jumlah byte yang ditampilkan, sehingga output lebih ringkas.
- Jika Anda sering bekerja dengan file biner, coba simpan perintah yang sering digunakan dalam skrip untuk efisiensi.