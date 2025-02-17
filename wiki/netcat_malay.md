# [Linux] Bash netcat Penggunaan: Alat untuk pemindahan data dan pengujian rangkaian

## Overview
Perintah `netcat`, sering dipanggil "nc", adalah alat yang sangat berguna dalam dunia pengurusan rangkaian. Ia membolehkan pengguna untuk membuat sambungan TCP atau UDP, menghantar dan menerima data, serta melakukan pengujian rangkaian dengan mudah. Netcat sering digunakan untuk debugging dan pemindahan fail.

## Usage
Sintaks asas untuk perintah netcat adalah seperti berikut:

```
netcat [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk netcat beserta penjelasan ringkas:

- `-l`: Mendengar sambungan masuk (listening mode).
- `-p`: Menentukan port yang akan digunakan.
- `-u`: Menggunakan protokol UDP.
- `-v`: Mengaktifkan mod verbose untuk maklumat tambahan.
- `-w`: Menentukan masa tamat untuk sambungan.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan netcat:

1. **Mendengar pada port tertentu:**
   ```bash
   nc -l -p 1234
   ```
   Perintah ini akan membuat netcat mendengar pada port 1234 untuk sambungan masuk.

2. **Menghantar fail melalui TCP:**
   ```bash
   nc -w 3 192.168.1.10 1234 < fail.txt
   ```
   Perintah ini menghantar fail `fail.txt` ke alamat IP 192.168.1.10 pada port 1234 dengan masa tamat 3 saat.

3. **Menerima fail:**
   ```bash
   nc -l -p 1234 > fail_diterima.txt
   ```
   Perintah ini akan mendengar pada port 1234 dan menyimpan data yang diterima ke dalam `fail_diterima.txt`.

4. **Menggunakan UDP:**
   ```bash
   echo "Hello, World!" | nc -u -w 1 192.168.1.10 1234
   ```
   Perintah ini menghantar mesej "Hello, World!" menggunakan protokol UDP ke alamat IP 192.168.1.10 pada port 1234.

## Tips
- Sentiasa gunakan mod verbose (`-v`) untuk mendapatkan maklumat tambahan semasa menyambung atau menghantar data.
- Gunakan `-w` untuk menetapkan masa tamat bagi sambungan, terutamanya jika anda berurusan dengan rangkaian yang tidak stabil.
- Pastikan firewall anda membenarkan sambungan pada port yang anda gunakan untuk mengelakkan masalah sambungan.