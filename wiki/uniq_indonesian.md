# [Sistem Operasi] C Shell (csh) uniq Penggunaan: Menghapus baris duplikat dari file

## Overview
Perintah `uniq` digunakan untuk menghapus baris-baris yang duplikat dari file atau output. Perintah ini hanya menghapus duplikat yang berurutan, sehingga penting untuk mengurutkan data terlebih dahulu jika ingin menghapus semua duplikat.

## Usage
Berikut adalah sintaks dasar dari perintah `uniq`:

```
uniq [options] [arguments]
```

## Common Options
- `-c`: Menghitung jumlah kemunculan setiap baris.
- `-d`: Menampilkan hanya baris yang muncul lebih dari sekali.
- `-u`: Menampilkan hanya baris yang unik (tidak ada duplikat).
- `-i`: Mengabaikan perbedaan antara huruf besar dan kecil saat membandingkan.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `uniq`:

1. Menghapus baris duplikat dari file:
   ```bash
   uniq file.txt
   ```

2. Mengurutkan file terlebih dahulu dan kemudian menghapus duplikat:
   ```bash
   sort file.txt | uniq
   ```

3. Menghitung jumlah kemunculan setiap baris:
   ```bash
   uniq -c file.txt
   ```

4. Menampilkan hanya baris yang muncul lebih dari sekali:
   ```bash
   uniq -d file.txt
   ```

5. Menampilkan hanya baris yang unik:
   ```bash
   uniq -u file.txt
   ```

## Tips
- Selalu urutkan data Anda sebelum menggunakan `uniq` jika Anda ingin menghapus semua duplikat.
- Gunakan opsi `-c` untuk mendapatkan informasi lebih lanjut tentang berapa kali setiap baris muncul.
- Jika Anda bekerja dengan data yang sensitif terhadap huruf besar dan kecil, pertimbangkan untuk menggunakan opsi `-i`.