# [Linux] Bash command penggunaan: Menampilkan isi file

## Overview
Perintah `cat` digunakan untuk menampilkan isi dari satu atau lebih file ke layar. Selain itu, `cat` juga dapat digunakan untuk menggabungkan file dan membuat file baru.

## Usage
Berikut adalah sintaks dasar dari perintah `cat`:

```
cat [options] [file...]
```

## Common Options
- `-n`: Menampilkan nomor baris pada output.
- `-b`: Menampilkan nomor baris hanya pada baris yang tidak kosong.
- `-E`: Menampilkan tanda `$` di akhir setiap baris.
- `-s`: Menghilangkan baris kosong yang berurutan.

## Common Examples
1. Menampilkan isi dari sebuah file:
   ```bash
   cat file.txt
   ```

2. Menampilkan isi dari beberapa file:
   ```bash
   cat file1.txt file2.txt
   ```

3. Menampilkan isi file dengan nomor baris:
   ```bash
   cat -n file.txt
   ```

4. Menggabungkan dua file dan menyimpan hasilnya ke file baru:
   ```bash
   cat file1.txt file2.txt > gabungan.txt
   ```

5. Menampilkan isi file dan menambahkan tanda `$` di akhir setiap baris:
   ```bash
   cat -E file.txt
   ```

## Tips
- Gunakan `cat` dengan hati-hati untuk file yang sangat besar, karena dapat mengeluarkan banyak data ke layar sekaligus.
- Untuk melihat isi file dengan lebih nyaman, pertimbangkan menggunakan `less` atau `more` untuk navigasi yang lebih baik.
- Anda dapat menggunakan `cat` untuk membuat file baru dengan mengarahkan input dari terminal:
  ```bash
  cat > file_baru.txt
  ```
  Setelah itu, ketikkan isi file dan tekan `CTRL+D` untuk menyimpan.