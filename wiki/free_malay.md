# [Linux] Bash free: Menunjukkan penggunaan memori

## Overview
Perintah `free` digunakan untuk memaparkan penggunaan memori dalam sistem Linux. Ia memberikan maklumat tentang jumlah memori yang digunakan, bebas, dan juga memori swap, membantu pengguna memahami status memori sistem mereka.

## Usage
Sintaks asas untuk perintah `free` adalah seperti berikut:

```
free [options] [arguments]
```

## Common Options
- `-h`: Menunjukkan penggunaan memori dalam format yang lebih mudah dibaca (contohnya, dalam MB atau GB).
- `-m`: Menunjukkan penggunaan memori dalam megabait.
- `-g`: Menunjukkan penggunaan memori dalam gigabait.
- `-s [seconds]`: Memaparkan maklumat memori secara berkala setiap beberapa saat yang ditentukan.
- `-t`: Menunjukkan jumlah keseluruhan memori.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `free`:

1. **Menunjukkan penggunaan memori dalam format yang mudah dibaca:**
   ```bash
   free -h
   ```

2. **Menunjukkan penggunaan memori dalam megabait:**
   ```bash
   free -m
   ```

3. **Menunjukkan penggunaan memori dalam gigabait:**
   ```bash
   free -g
   ```

4. **Menunjukkan maklumat memori setiap 5 saat:**
   ```bash
   free -s 5
   ```

5. **Menunjukkan jumlah keseluruhan memori:**
   ```bash
   free -t
   ```

## Tips
- Gunakan pilihan `-h` untuk mendapatkan maklumat yang lebih mudah dibaca, terutamanya jika anda tidak biasa dengan angka besar.
- Perintah `free` boleh digabungkan dengan perintah lain seperti `grep` untuk menapis maklumat tertentu.
- Untuk pemantauan berterusan, pertimbangkan menggunakan pilihan `-s` bersama dengan `watch` untuk melihat perubahan dalam penggunaan memori secara langsung.