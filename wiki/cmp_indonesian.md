# [Sistem Operasi] C Shell (csh) cmp Penggunaan: Membandingkan dua file

## Overview
Perintah `cmp` digunakan untuk membandingkan dua file byte demi byte. Jika file yang dibandingkan berbeda, `cmp` akan menunjukkan lokasi perbedaan tersebut. Jika file identik, tidak ada output yang dihasilkan.

## Usage
Berikut adalah sintaks dasar dari perintah `cmp`:

```bash
cmp [options] [arguments]
```

## Common Options
- `-l`: Menampilkan byte yang berbeda dalam format numerik.
- `-s`: Menyembunyikan output dan hanya mengembalikan status exit.
- `-i <n>`: Mengabaikan n byte pertama dari setiap file.
- `-n <n>`: Membandingkan hanya n byte pertama dari file.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `cmp`:

1. Membandingkan dua file dan menampilkan perbedaan:
   ```bash
   cmp file1.txt file2.txt
   ```

2. Menggunakan opsi `-l` untuk menampilkan byte yang berbeda:
   ```bash
   cmp -l file1.txt file2.txt
   ```

3. Menggunakan opsi `-s` untuk membandingkan tanpa output:
   ```bash
   cmp -s file1.txt file2.txt
   ```

4. Mengabaikan n byte pertama dari file saat membandingkan:
   ```bash
   cmp -i 10 file1.txt file2.txt
   ```

5. Membandingkan hanya n byte pertama dari file:
   ```bash
   cmp -n 20 file1.txt file2.txt
   ```

## Tips
- Gunakan opsi `-s` jika Anda hanya ingin mengetahui apakah file berbeda tanpa melihat detailnya.
- Opsi `-l` sangat berguna untuk debugging, karena memberikan informasi spesifik tentang byte yang berbeda.
- Pastikan untuk memeriksa status exit dari perintah `cmp` untuk menentukan apakah file identik atau tidak. Status exit `0` berarti file identik, `1` berarti berbeda, dan `2` menunjukkan kesalahan.