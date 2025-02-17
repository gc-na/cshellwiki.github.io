# [Linux] Bash split Penggunaan: Memecah fail kepada bahagian yang lebih kecil

## Overview
Perintah `split` dalam Bash digunakan untuk memecah fail besar kepada beberapa bahagian yang lebih kecil. Ini berguna apabila anda ingin menguruskan fail yang terlalu besar untuk diproses sekaligus.

## Usage
Berikut adalah sintaks asas untuk perintah `split`:

```bash
split [options] [arguments]
```

## Common Options
- `-l NUM`: Memecah fail kepada bahagian yang mempunyai NUM baris setiap satu.
- `-b SIZE`: Memecah fail kepada bahagian dengan saiz tertentu (contohnya, `1M` untuk 1 megabait).
- `-d`: Menggunakan angka sebagai penama bagi fail yang dihasilkan.
- `--additional-suffix=SUFFIX`: Menambah suffix tambahan pada nama fail yang dihasilkan.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `split`:

1. Memecah fail kepada bahagian 100 baris setiap satu:
   ```bash
   split -l 100 myfile.txt
   ```

2. Memecah fail kepada bahagian 1 megabait setiap satu:
   ```bash
   split -b 1M mylargefile.dat
   ```

3. Memecah fail dan menggunakan angka untuk penamaan fail:
   ```bash
   split -d -l 50 myfile.txt part_
   ```

4. Memecah fail dengan suffix tambahan:
   ```bash
   split --additional-suffix=.txt -l 30 myfile.txt part_
   ```

## Tips
- Sentiasa semak saiz fail yang dihasilkan untuk memastikan ia sesuai dengan keperluan anda.
- Gunakan pilihan `-d` jika anda ingin memudahkan pengenalan fail yang dihasilkan.
- Jika anda merancang untuk menggabungkan semula fail, pastikan untuk menggunakan penamaan yang konsisten.