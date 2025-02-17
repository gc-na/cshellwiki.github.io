# [Linux] Bash tee Penggunaan: Menyalin dan Menulis ke Fail

## Overview
Perintah `tee` dalam Bash digunakan untuk membaca dari input standard dan menulis ke output standard serta satu atau lebih fail. Ini membolehkan pengguna untuk melihat output pada skrin sambil juga menyimpannya ke dalam fail.

## Usage
Sintaks asas untuk perintah `tee` adalah seperti berikut:

```bash
tee [options] [arguments]
```

## Common Options
- `-a`, `--append`: Menambah output ke fail yang sedia ada, bukannya menulis semula.
- `-i`, `--ignore-interrupts`: Mengabaikan isyarat interrupt.
- `-p`, `--output-error`: Menentukan bagaimana untuk menangani ralat output.

## Common Examples

1. **Menulis output ke dalam fail**:
   ```bash
   echo "Hello, World!" | tee output.txt
   ```
   Perintah ini akan menulis "Hello, World!" ke dalam fail `output.txt` dan juga memaparkannya di skrin.

2. **Menambah output ke dalam fail sedia ada**:
   ```bash
   echo "New line" | tee -a output.txt
   ```
   Ini akan menambah "New line" ke dalam `output.txt` tanpa menghapuskan isi yang sedia ada.

3. **Menulis output ke beberapa fail**:
   ```bash
   echo "Data" | tee file1.txt file2.txt
   ```
   Perintah ini akan menulis "Data" ke dalam `file1.txt` dan `file2.txt` serta memaparkannya di skrin.

4. **Menggunakan tee dalam pipeline**:
   ```bash
   ls -l | tee list.txt | grep "txt"
   ```
   Di sini, output dari `ls -l` akan disimpan dalam `list.txt` dan juga diproses oleh `grep` untuk mencari fail yang mengandungi "txt".

## Tips
- Gunakan pilihan `-a` jika anda ingin menambah data ke dalam fail tanpa menghapuskan data yang sedia ada.
- Pastikan anda mempunyai izin untuk menulis ke fail yang dituju.
- `tee` sangat berguna dalam skrip untuk menyimpan log output sambil memaparkannya di konsol.