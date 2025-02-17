# [Linux] Bash if: Memeriksa kondisi

## Overview
Perintah `if` dalam Bash digunakan untuk mengevaluasi kondisi dan menjalankan perintah tertentu berdasarkan hasil evaluasi tersebut. Ini memungkinkan pengguna untuk membuat keputusan dalam skrip berdasarkan nilai yang diberikan.

## Usage
Sintaks dasar dari perintah `if` adalah sebagai berikut:

```bash
if [ kondisi ]; then
    perintah
fi
```

## Common Options
Berikut adalah beberapa opsi umum yang digunakan dengan perintah `if`:

- `-e`: Memeriksa apakah file ada.
- `-d`: Memeriksa apakah direktori ada.
- `-f`: Memeriksa apakah file adalah file biasa.
- `-z`: Memeriksa apakah panjang string adalah nol.
- `-n`: Memeriksa apakah panjang string tidak nol.

## Common Examples

1. **Memeriksa keberadaan file:**
   ```bash
   if [ -e "file.txt" ]; then
       echo "File ada."
   else
       echo "File tidak ada."
   fi
   ```

2. **Memeriksa apakah direktori ada:**
   ```bash
   if [ -d "folder" ]; then
       echo "Folder ada."
   else
       echo "Folder tidak ada."
   fi
   ```

3. **Memeriksa string kosong:**
   ```bash
   my_string=""
   if [ -z "$my_string" ]; then
       echo "String kosong."
   else
       echo "String tidak kosong."
   fi
   ```

4. **Menggunakan kondisi numerik:**
   ```bash
   num=10
   if [ $num -gt 5 ]; then
       echo "Num lebih besar dari 5."
   else
       echo "Num tidak lebih besar dari 5."
   fi
   ```

## Tips
- Selalu gunakan spasi yang tepat di dalam tanda kurung siku `[ ]` untuk menghindari kesalahan sintaks.
- Gunakan `elif` untuk menambahkan lebih banyak kondisi dalam pernyataan `if`.
- Pastikan untuk menutup pernyataan `if` dengan `fi` untuk menghindari kebingungan dalam skrip.