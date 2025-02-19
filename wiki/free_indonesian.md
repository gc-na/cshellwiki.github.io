# [Linux] C Shell (csh) free: Menampilkan informasi penggunaan memori

## Overview
Perintah `free` digunakan untuk menampilkan informasi tentang penggunaan memori di sistem. Ini memberikan gambaran umum tentang memori fisik dan swap yang tersedia serta yang sedang digunakan.

## Usage
Sintaks dasar dari perintah `free` adalah sebagai berikut:

```
free [options] [arguments]
```

## Common Options
- `-h`: Menampilkan ukuran dalam format yang lebih mudah dibaca (misalnya, KB, MB, GB).
- `-m`: Menampilkan ukuran dalam megabyte.
- `-g`: Menampilkan ukuran dalam gigabyte.
- `-s <interval>`: Menampilkan informasi memori secara berkala setiap interval detik yang ditentukan.
- `-t`: Menampilkan total penggunaan memori.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `free`:

1. Menampilkan informasi memori dalam format yang lebih mudah dibaca:
   ```csh
   free -h
   ```

2. Menampilkan informasi memori dalam megabyte:
   ```csh
   free -m
   ```

3. Menampilkan informasi memori dalam gigabyte:
   ```csh
   free -g
   ```

4. Menampilkan informasi memori setiap 5 detik:
   ```csh
   free -s 5
   ```

5. Menampilkan total penggunaan memori:
   ```csh
   free -t
   ```

## Tips
- Gunakan opsi `-h` untuk mendapatkan tampilan yang lebih ramah pengguna saat memeriksa penggunaan memori.
- Menggunakan opsi `-s` dapat membantu dalam memantau penggunaan memori secara real-time, sangat berguna saat melakukan troubleshooting.
- Perhatikan perbedaan antara memori yang digunakan dan memori yang tersedia untuk memahami kesehatan sistem Anda.