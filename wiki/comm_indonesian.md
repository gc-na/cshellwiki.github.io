# [Linux] Bash comm: membandingkan dua file baris

## Overview
Perintah `comm` digunakan untuk membandingkan dua file teks yang sudah diurutkan. Perintah ini akan menampilkan tiga kolom: baris yang hanya ada di file pertama, baris yang hanya ada di file kedua, dan baris yang ada di kedua file.

## Usage
Sintaks dasar dari perintah `comm` adalah sebagai berikut:

```bash
comm [options] [file1] [file2]
```

## Common Options
- `-1`: Menghilangkan kolom pertama (baris yang hanya ada di file pertama).
- `-2`: Menghilangkan kolom kedua (baris yang hanya ada di file kedua).
- `-3`: Menghilangkan kolom ketiga (baris yang ada di kedua file).
- `-i`: Mengabaikan perbedaan huruf besar dan kecil saat membandingkan.
- `-u`: Menampilkan hanya baris unik dari kedua file.

## Common Examples

1. **Membandingkan dua file**:
   ```bash
   comm file1.txt file2.txt
   ```

2. **Menghilangkan kolom pertama**:
   ```bash
   comm -1 file1.txt file2.txt
   ```

3. **Mengabaikan perbedaan huruf besar dan kecil**:
   ```bash
   comm -i file1.txt file2.txt
   ```

4. **Menampilkan hanya baris unik dari kedua file**:
   ```bash
   comm -u file1.txt file2.txt
   ```

## Tips
- Pastikan kedua file yang akan dibandingkan sudah diurutkan, karena `comm` hanya berfungsi dengan file yang terurut.
- Gunakan opsi `-i` jika Anda ingin membandingkan file tanpa memperhatikan huruf besar dan kecil.
- Untuk analisis yang lebih mendalam, pertimbangkan untuk menggabungkan `comm` dengan perintah lain seperti `sort` untuk memastikan file Anda terurut sebelum dibandingkan.