# [Linux] Bash tac Penggunaan: Membalikkan baris dalam fail

## Overview
Perintah `tac` dalam Bash digunakan untuk membalikkan urutan baris dalam satu atau lebih fail. Ia berfungsi dengan cara yang sama seperti perintah `cat`, tetapi dengan cara yang terbalik, menjadikan baris terakhir menjadi baris pertama.

## Usage
Berikut adalah sintaks asas untuk perintah `tac`:

```bash
tac [options] [arguments]
```

## Common Options
- `-b`, `--before`: Menambah pemisah sebelum setiap baris.
- `-r`, `--regex`: Menggunakan ungkapan biasa untuk pemisah.
- `-s`, `--separator`: Menentukan pemisah yang digunakan antara baris.

## Common Examples

1. **Membalikkan fail teks:**
   Untuk membalikkan semua baris dalam fail `contoh.txt`, gunakan perintah berikut:
   ```bash
   tac contoh.txt
   ```

2. **Membalikkan fail dan menyimpan output ke fail baru:**
   Anda boleh membalikkan fail dan menyimpannya ke dalam fail baru dengan menggunakan pengalihan:
   ```bash
   tac contoh.txt > contoh_balik.txt
   ```

3. **Membalikkan baris dengan pemisah khusus:**
   Jika anda ingin membalikkan fail dengan pemisah tertentu, contohnya koma, gunakan:
   ```bash
   tac -s ',' contoh.txt
   ```

4. **Menggunakan ungkapan biasa untuk pemisah:**
   Untuk membalikkan fail dengan menggunakan ungkapan biasa, anda boleh melakukan:
   ```bash
   tac -r -s '[[:space:]]' contoh.txt
   ```

## Tips
- Pastikan untuk memeriksa fail yang anda ingin balikkan, kerana `tac` tidak mengubah fail asal, tetapi hanya memberikan output yang terbalik.
- Gunakan pengalihan output untuk menyimpan hasil ke dalam fail baru jika anda ingin menyimpan perubahan.
- `tac` sangat berguna dalam pemprosesan data dan analisis log, di mana anda mungkin ingin melihat entri terbaru terlebih dahulu.