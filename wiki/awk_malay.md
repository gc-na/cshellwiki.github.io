# [Linux] Bash awk Penggunaan: Memproses dan Menganalisis Teks

## Overview
Perintah `awk` adalah alat pemrograman yang kuat dalam Bash yang digunakan untuk memproses dan menganalisis teks. Ia sering digunakan untuk mengekstrak dan memanipulasi data dari fail teks, terutamanya dalam format yang terstruktur seperti CSV.

## Usage
Sintaks asas untuk menggunakan `awk` adalah seperti berikut:

```bash
awk [options] [arguments]
```

## Common Options
- `-F`: Menetapkan pemisah input. Contohnya, `-F,` untuk fail CSV.
- `-v`: Menggunakan pembolehubah untuk menghantar nilai ke dalam skrip awk.
- `-f`: Menggunakan fail skrip awk yang ditetapkan.
- `-W`: Mengaktifkan pilihan tertentu yang tidak ada dalam versi standard awk.

## Common Examples
Berikut adalah beberapa contoh penggunaan `awk`:

1. **Mengeluarkan kolum tertentu dari fail teks:**
   ```bash
   awk '{print $1}' fail.txt
   ```
   Perintah ini akan mencetak kolum pertama dari `fail.txt`.

2. **Menggunakan pemisah untuk fail CSV:**
   ```bash
   awk -F, '{print $2}' data.csv
   ```
   Ini akan mencetak kolum kedua dari `data.csv` yang dipisahkan dengan koma.

3. **Menghitung jumlah baris dalam fail:**
   ```bash
   awk 'END {print NR}' fail.txt
   ```
   Perintah ini mencetak jumlah baris dalam `fail.txt`.

4. **Menyaring baris berdasarkan kriteria tertentu:**
   ```bash
   awk '$3 > 50' data.txt
   ```
   Ini akan mencetak semua baris di mana nilai dalam kolum ketiga lebih besar daripada 50.

5. **Menggunakan pembolehubah:**
   ```bash
   awk -v threshold=100 '$2 > threshold' data.txt
   ```
   Perintah ini mencetak baris di mana nilai dalam kolum kedua melebihi nilai yang ditetapkan dalam pembolehubah `threshold`.

## Tips
- Gunakan `awk` bersama dengan `grep` untuk penyaringan yang lebih kompleks.
- Sentiasa tentukan pemisah dengan `-F` jika anda bekerja dengan data yang dipisahkan oleh tanda tertentu.
- Manfaatkan pembolehubah untuk membuat skrip awk lebih dinamik dan mudah dibaca.