# [Linux] Bash pr: [mengatur tampilan file teks]

## Overview
Perintah `pr` dalam Bash digunakan untuk memformat file teks agar lebih mudah dibaca. Ini sering digunakan untuk menyiapkan dokumen untuk dicetak dengan mengatur kolom, menambahkan header, dan mengatur margin.

## Usage
Berikut adalah sintaks dasar dari perintah `pr`:

```
pr [options] [arguments]
```

## Common Options
- `-h`: Menambahkan header khusus.
- `-l`: Menentukan jumlah baris per halaman.
- `-w`: Menentukan lebar halaman dalam karakter.
- `-s`: Mengatur spasi antara kolom.
- `-t`: Mengabaikan header dan footer default.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `pr`:

1. **Mencetak file teks dengan format default:**
   ```bash
   pr file.txt
   ```

2. **Menentukan lebar halaman menjadi 80 karakter:**
   ```bash
   pr -w 80 file.txt
   ```

3. **Menambahkan header khusus:**
   ```bash
   pr -h "Laporan Bulanan" file.txt
   ```

4. **Mengatur jumlah baris per halaman menjadi 50:**
   ```bash
   pr -l 50 file.txt
   ```

5. **Mengabaikan header dan footer default:**
   ```bash
   pr -t file.txt
   ```

## Tips
- Gunakan opsi `-h` untuk menambahkan informasi penting di bagian atas dokumen.
- Pastikan untuk menyesuaikan lebar halaman dengan ukuran kertas yang akan digunakan untuk mencetak.
- Cobalah menggabungkan beberapa opsi untuk mendapatkan format yang diinginkan, misalnya, `pr -h "Judul" -w 80 -l 60 file.txt`.