# [Linux] Bash script Penggunaan: Merekod sesi terminal

## Overview
Perintah `script` digunakan untuk merekod sesi terminal ke dalam fail. Ia membolehkan pengguna menyimpan semua output yang dihasilkan semasa sesi terminal, termasuk input yang dimasukkan oleh pengguna. Ini berguna untuk dokumentasi, pengajaran, atau untuk menyimpan hasil kerja.

## Usage
Berikut adalah sintaks asas untuk perintah `script`:

```bash
script [options] [arguments]
```

## Common Options
- `-a`: Menambah output ke fail yang sedia ada, bukannya menulis semula.
- `-f`: Menunjukkan output secara langsung ke terminal semasa merekod.
- `-q`: Menjalankan dalam mod senyap, tanpa mesej permulaan dan akhir.
- `[filename]`: Nama fail untuk menyimpan output. Jika tidak ditentukan, output akan disimpan dalam `typescript`.

## Common Examples

1. **Merekod sesi terminal ke dalam fail:**
   ```bash
   script mysession.txt
   ```
   Ini akan memulakan sesi baru dan menyimpan semua output ke dalam `mysession.txt`.

2. **Merekod sesi dan menambah ke fail sedia ada:**
   ```bash
   script -a mysession.txt
   ```
   Menggunakan pilihan `-a` untuk menambah output ke `mysession.txt` tanpa menimpa data yang sedia ada.

3. **Merekod sesi dengan output langsung:**
   ```bash
   script -f mysession.txt
   ```
   Dengan pilihan `-f`, output akan dipaparkan secara langsung di terminal semasa sesi direkod.

4. **Menjalankan dalam mod senyap:**
   ```bash
   script -q mysession.txt
   ```
   Ini akan merekod sesi tanpa sebarang mesej permulaan atau akhir.

## Tips
- Sentiasa semak fail output selepas sesi untuk memastikan semua maklumat yang diperlukan telah direkod.
- Gunakan pilihan `-f` jika anda ingin melihat output secara langsung semasa sesi.
- Untuk sesi yang panjang, pertimbangkan untuk menggunakan pilihan `-a` agar tidak kehilangan maklumat yang telah direkod sebelum ini.