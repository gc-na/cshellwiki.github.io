# [Linux] Bash cmp Penggunaan: Membandingkan dua fail

## Overview
Perintah `cmp` dalam Bash digunakan untuk membandingkan dua fail byte demi byte. Ia berguna untuk menentukan sama ada dua fail adalah sama atau berbeza, dan jika berbeza, ia juga menunjukkan lokasi perbezaan tersebut.

## Usage
Berikut adalah sintaks asas untuk perintah `cmp`:

```
cmp [options] [arguments]
```

## Common Options
- `-l`: Menunjukkan perbezaan dalam bentuk nombor byte dan nilai byte.
- `-s`: Menghasilkan output yang tidak menunjukkan perbezaan, hanya memberikan kod keluar.
- `-i OFFSET`: Mengabaikan `OFFSET` byte pertama dari setiap fail semasa membandingkan.
- `-n N`: Membandingkan hanya `N` byte pertama dari fail.

## Common Examples

1. **Membandingkan dua fail**:
   ```bash
   cmp file1.txt file2.txt
   ```

2. **Menggunakan pilihan -s untuk senyap**:
   ```bash
   cmp -s file1.txt file2.txt
   if [ $? -eq 0 ]; then
       echo "Fail adalah sama."
   else
       echo "Fail adalah berbeza."
   fi
   ```

3. **Menunjukkan perbezaan dalam format nombor byte**:
   ```bash
   cmp -l file1.txt file2.txt
   ```

4. **Membandingkan hanya beberapa byte pertama**:
   ```bash
   cmp -n 10 file1.txt file2.txt
   ```

## Tips
- Gunakan pilihan `-s` jika anda hanya ingin tahu sama ada fail adalah sama tanpa output terperinci.
- Untuk fail yang besar, pertimbangkan untuk menggunakan pilihan `-n` untuk membandingkan hanya bahagian tertentu yang anda minati.
- Sentiasa semak kod keluar (`$?`) selepas menjalankan `cmp` untuk mendapatkan maklumat tentang hasil perbandingan.