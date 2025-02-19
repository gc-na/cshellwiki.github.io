# [Sistem Operasi] C Shell (csh) script Penggunaan: Merekam sesi terminal

## Overview
Perintah `script` digunakan untuk merekam sesi terminal ke dalam sebuah file. Ini sangat berguna untuk mencatat semua perintah yang dijalankan dan output yang dihasilkan selama sesi tersebut, sehingga Anda dapat mereview atau membagikannya di kemudian hari.

## Usage
Berikut adalah sintaks dasar dari perintah `script`:

```
script [options] [arguments]
```

## Common Options
- `-a`: Menambahkan output ke file yang sudah ada, bukan menimpanya.
- `-f`: Menampilkan output ke terminal secara langsung saat merekam.
- `-q`: Menjalankan dalam mode senyap, tanpa menampilkan pesan pembuka.
- `-t`: Merekam waktu yang dibutuhkan untuk setiap perintah yang dijalankan.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `script`:

1. Merekam sesi terminal ke dalam file bernama `output.txt`:
   ```bash
   script output.txt
   ```

2. Merekam sesi terminal dan menambahkan output ke file yang sudah ada:
   ```bash
   script -a output.txt
   ```

3. Merekam sesi terminal dengan tampilan langsung ke terminal:
   ```bash
   script -f output.txt
   ```

4. Menjalankan `script` dalam mode senyap:
   ```bash
   script -q output.txt
   ```

5. Merekam waktu untuk setiap perintah yang dijalankan:
   ```bash
   script -t output.txt
   ```

## Tips
- Pastikan untuk menghentikan sesi `script` dengan mengetik `exit` atau `Ctrl+D` agar file hasil rekaman tersimpan dengan benar.
- Gunakan opsi `-a` jika Anda ingin merekam beberapa sesi ke dalam file yang sama tanpa kehilangan data sebelumnya.
- Periksa file hasil rekaman dengan menggunakan perintah `cat` atau `less` untuk melihat isi dari sesi yang telah direkam.