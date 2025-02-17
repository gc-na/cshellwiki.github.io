# [Linux] Bash uniq Penggunaan: Menghapus baris duplikat dalam fail

## Overview
Perintah `uniq` dalam Bash digunakan untuk menghapus baris yang berulang dalam fail atau output. Ia hanya berfungsi pada baris yang bersebelahan, jadi biasanya digunakan bersama dengan perintah lain seperti `sort` untuk memastikan baris yang sama berada bersebelahan sebelum diproses.

## Usage
Berikut adalah sintaks asas untuk perintah `uniq`:

```
uniq [options] [arguments]
```

## Common Options
- `-c`: Mengira bilangan kemunculan setiap baris.
- `-d`: Menunjukkan hanya baris yang duplikat.
- `-u`: Menunjukkan hanya baris yang unik.
- `-i`: Mengabaikan kes (case insensitive) semasa membandingkan baris.
- `-w N`: Mengabaikan N karakter pertama dalam perbandingan.

## Common Examples
Berikut adalah beberapa contoh penggunaan `uniq`:

1. **Menghapus baris duplikat dalam fail:**
   ```bash
   sort fail.txt | uniq
   ```

2. **Mengira bilangan kemunculan setiap baris:**
   ```bash
   sort fail.txt | uniq -c
   ```

3. **Menunjukkan hanya baris yang duplikat:**
   ```bash
   sort fail.txt | uniq -d
   ```

4. **Menunjukkan hanya baris yang unik:**
   ```bash
   sort fail.txt | uniq -u
   ```

5. **Mengabaikan kes semasa membandingkan:**
   ```bash
   sort fail.txt | uniq -i
   ```

6. **Mengabaikan N karakter pertama:**
   ```bash
   sort fail.txt | uniq -w 5
   ```

## Tips
- Sentiasa gunakan `sort` sebelum `uniq` untuk memastikan baris yang sama berada bersebelahan.
- Gunakan pilihan `-c` untuk mendapatkan gambaran tentang berapa kali setiap baris muncul, yang boleh membantu dalam analisis data.
- Jika anda bekerja dengan fail besar, pertimbangkan untuk menggunakan `uniq` dengan pilihan `-w` untuk fokus pada bahagian tertentu dari baris.