# [Linux] Bash uniq Penggunaan: Menghapus baris duplikat

## Overview
Perintah `uniq` dalam Bash digunakan untuk menghapus baris yang duplikat dari file atau input standar. Perintah ini sangat berguna ketika Anda ingin mendapatkan daftar unik dari data yang mungkin memiliki entri yang sama.

## Usage
Berikut adalah sintaks dasar dari perintah `uniq`:

```
uniq [options] [arguments]
```

## Common Options
Beberapa opsi umum yang dapat digunakan dengan `uniq` antara lain:

- `-c`: Menghitung jumlah kemunculan setiap baris.
- `-d`: Menampilkan hanya baris yang muncul lebih dari sekali.
- `-u`: Menampilkan hanya baris yang unik (tidak ada duplikat).
- `-i`: Mengabaikan perbedaan huruf besar/kecil saat membandingkan baris.

## Common Examples

1. **Menghapus baris duplikat dari file:**
   ```bash
   uniq file.txt
   ```

2. **Menghitung jumlah kemunculan setiap baris:**
   ```bash
   uniq -c file.txt
   ```

3. **Menampilkan hanya baris yang muncul lebih dari sekali:**
   ```bash
   uniq -d file.txt
   ```

4. **Menampilkan hanya baris yang unik:**
   ```bash
   uniq -u file.txt
   ```

5. **Menggunakan uniq dengan sort untuk menghapus duplikat dari output yang tidak terurut:**
   ```bash
   sort file.txt | uniq
   ```

## Tips
- Pastikan untuk mengurutkan file terlebih dahulu jika Anda ingin menghapus duplikat secara efektif, karena `uniq` hanya menghapus baris yang berurutan.
- Gunakan opsi `-i` jika Anda ingin mengabaikan perbedaan huruf besar/kecil saat membandingkan baris.
- Kombinasikan `uniq` dengan perintah lain seperti `sort` untuk memproses data dengan lebih efisien.