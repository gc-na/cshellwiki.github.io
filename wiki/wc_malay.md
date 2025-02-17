# [Linux] Bash wc Penggunaan: Mengira baris, kata, dan aksara dalam fail

## Overview
Perintah `wc` (word count) dalam Bash digunakan untuk mengira jumlah baris, kata, dan aksara dalam satu atau lebih fail. Ia sangat berguna untuk mendapatkan statistik ringkas tentang kandungan fail teks.

## Usage
Sintaks asas untuk perintah `wc` adalah seperti berikut:

```
wc [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk perintah `wc`:

- `-l`: Mengira jumlah baris dalam fail.
- `-w`: Mengira jumlah kata dalam fail.
- `-c`: Mengira jumlah aksara dalam fail.
- `-m`: Mengira jumlah aksara (termasuk aksara Unicode).
- `-L`: Menunjukkan panjang baris terpanjang dalam fail.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan perintah `wc`:

1. Mengira jumlah baris dalam fail:
   ```bash
   wc -l fail.txt
   ```

2. Mengira jumlah kata dalam fail:
   ```bash
   wc -w fail.txt
   ```

3. Mengira jumlah aksara dalam fail:
   ```bash
   wc -c fail.txt
   ```

4. Mengira jumlah baris, kata, dan aksara sekaligus:
   ```bash
   wc fail.txt
   ```

5. Mengira panjang baris terpanjang dalam fail:
   ```bash
   wc -L fail.txt
   ```

## Tips
- Anda boleh menggunakan `wc` bersama dengan perintah lain menggunakan paip (`|`) untuk mengira hasil output. Contohnya, untuk mengira jumlah fail dalam direktori:
  ```bash
  ls | wc -l
  ```
- Untuk mengira beberapa fail sekaligus, anda boleh menyenaraikan semua fail dalam arahan:
  ```bash
  wc fail1.txt fail2.txt
  ```
- Gunakan pilihan `-h` untuk mendapatkan output yang lebih mudah dibaca, terutama untuk fail yang besar.