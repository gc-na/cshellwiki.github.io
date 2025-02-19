# [Sistem Operasi] C Shell (csh) comm: Membandingkan dua file baris

## Overview
Perintah `comm` digunakan untuk membandingkan dua file yang diurutkan dan menampilkan baris yang berbeda dan sama antara keduanya. Ini sangat berguna untuk melihat perbedaan antara dua daftar atau file teks.

## Usage
Berikut adalah sintaks dasar dari perintah `comm`:

```csh
comm [options] [arguments]
```

## Common Options
- `-1`: Mengabaikan kolom pertama (baris yang hanya ada di file pertama).
- `-2`: Mengabaikan kolom kedua (baris yang hanya ada di file kedua).
- `-3`: Mengabaikan kolom ketiga (baris yang ada di kedua file).
- `-i`: Mengabaikan perbedaan huruf besar dan kecil saat membandingkan.
- `-u`: Menampilkan output dalam urutan tidak terurut.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `comm`:

1. **Membandingkan dua file dan menampilkan semua kolom:**
   ```csh
   comm file1.txt file2.txt
   ```

2. **Mengabaikan baris yang hanya ada di file pertama:**
   ```csh
   comm -1 file1.txt file2.txt
   ```

3. **Mengabaikan baris yang hanya ada di file kedua:**
   ```csh
   comm -2 file1.txt file2.txt
   ```

4. **Mengabaikan perbedaan huruf besar dan kecil:**
   ```csh
   comm -i file1.txt file2.txt
   ```

5. **Menampilkan hanya baris yang ada di kedua file:**
   ```csh
   comm -3 file1.txt file2.txt
   ```

## Tips
- Pastikan kedua file yang ingin dibandingkan sudah diurutkan. Jika tidak, hasilnya mungkin tidak akurat.
- Gunakan opsi `-i` jika Anda ingin mengabaikan perbedaan huruf besar dan kecil, terutama saat bekerja dengan teks yang tidak konsisten.
- Untuk analisis yang lebih mendalam, pertimbangkan untuk menggabungkan `comm` dengan perintah lain seperti `sort` untuk memastikan file Anda terurut sebelum dibandingkan.