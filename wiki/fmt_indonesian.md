# [Linux] Bash fmt Penggunaan: Mengatur Format Teks

## Overview
Perintah `fmt` digunakan untuk memformat teks dengan cara mengatur lebar baris dan merapikan teks agar lebih mudah dibaca. Ini sangat berguna untuk mengubah teks yang tidak terformat menjadi format yang lebih terstruktur.

## Usage
Berikut adalah sintaks dasar dari perintah `fmt`:

```bash
fmt [options] [arguments]
```

## Common Options
- `-w <width>`: Menentukan lebar maksimum baris yang diinginkan (default adalah 75 karakter).
- `-s`: Mengabaikan spasi ganda, menjaga jarak antar kata tetap satu spasi.
- `-u`: Mengatur teks menjadi justified (rata kanan dan kiri).

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `fmt`:

1. **Memformat file teks dengan lebar default:**
   ```bash
   fmt myfile.txt
   ```

2. **Memformat teks dengan lebar 50 karakter:**
   ```bash
   fmt -w 50 myfile.txt
   ```

3. **Mengabaikan spasi ganda dalam teks:**
   ```bash
   fmt -s myfile.txt
   ```

4. **Mengatur teks menjadi justified:**
   ```bash
   fmt -u myfile.txt
   ```

5. **Menggunakan fmt dengan output ke file baru:**
   ```bash
   fmt myfile.txt > formatted.txt
   ```

## Tips
- Selalu periksa lebar baris yang sesuai untuk jenis dokumen yang Anda kerjakan agar teks tetap mudah dibaca.
- Gunakan opsi `-s` jika Anda bekerja dengan teks yang memiliki banyak spasi ganda untuk menjaga kebersihan format.
- Cobalah berbagai kombinasi opsi untuk melihat hasil yang paling sesuai dengan kebutuhan Anda.