# [Linux] Bash tr <Penggunaan setara>: Mengubah karakter dalam teks

## Overview
Perintah `tr` dalam Bash digunakan untuk mentransformasikan karakter dalam input. Ini sering digunakan untuk mengganti, menghapus, atau mengubah karakter tertentu dalam teks.

## Usage
Sintaks dasar dari perintah `tr` adalah sebagai berikut:

```
tr [options] [arguments]
```

## Common Options
- `-d`: Menghapus karakter yang ditentukan.
- `-s`: Mengganti karakter berulang dengan satu karakter.
- `-c`: Menggunakan karakter yang tidak ditentukan.
- `-t`: Mengubah karakter dari satu set ke set lainnya.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `tr`:

1. **Mengganti huruf kecil dengan huruf besar:**
   ```bash
   echo "hello world" | tr 'a-z' 'A-Z'
   ```

2. **Menghapus angka dari teks:**
   ```bash
   echo "abc123def456" | tr -d '0-9'
   ```

3. **Mengganti spasi berulang dengan satu spasi:**
   ```bash
   echo "This    is    a    test." | tr -s ' '
   ```

4. **Mengubah karakter tertentu:**
   ```bash
   echo "apple, banana, cherry" | tr ',' ';'
   ```

## Tips
- Selalu gunakan tanda kutip untuk menghindari masalah dengan karakter khusus.
- Kombinasikan `tr` dengan perintah lain menggunakan pipe (`|`) untuk memproses data secara efisien.
- Periksa hasil output dengan menggunakan `cat -e` untuk melihat karakter akhir baris jika diperlukan.