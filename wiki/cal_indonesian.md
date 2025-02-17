# [Linux] Bash cal Penggunaan: Menampilkan Kalender

## Overview
Perintah `cal` digunakan untuk menampilkan kalender di terminal. Dengan `cal`, pengguna dapat melihat kalender bulanan atau tahunan, serta informasi tambahan seperti hari libur.

## Usage
Sintaks dasar dari perintah `cal` adalah sebagai berikut:

```bash
cal [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan perintah `cal`:

- `-m`: Menampilkan kalender dengan nama bulan di atas.
- `-y`: Menampilkan kalender untuk tahun saat ini.
- `-3`: Menampilkan kalender untuk bulan ini, bulan sebelumnya, dan bulan berikutnya.
- `-j`: Menampilkan hari dalam tahun (Julian).
- `-w`: Menampilkan minggu yang dimulai pada hari Minggu.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `cal`:

1. Menampilkan kalender bulan ini:
   ```bash
   cal
   ```

2. Menampilkan kalender untuk bulan tertentu (misalnya, Maret 2023):
   ```bash
   cal 03 2023
   ```

3. Menampilkan kalender untuk tahun tertentu (misalnya, 2023):
   ```bash
   cal -y 2023
   ```

4. Menampilkan kalender untuk bulan ini, bulan sebelumnya, dan bulan berikutnya:
   ```bash
   cal -3
   ```

5. Menampilkan kalender dengan hari dalam tahun (Julian):
   ```bash
   cal -j
   ```

## Tips
- Gunakan opsi `-m` untuk menampilkan nama bulan yang lebih jelas.
- Cobalah opsi `-3` untuk mendapatkan gambaran yang lebih luas tentang bulan yang sedang berlangsung.
- Untuk melihat kalender dengan format yang lebih ringkas, pertimbangkan untuk menggunakan opsi `-w` jika Anda lebih suka minggu dimulai pada hari Minggu.