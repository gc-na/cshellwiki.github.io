# [Linux] Bash tee Penggunaan: Menyalin dan Mengalirkan Output

## Overview
Perintah `tee` dalam Bash digunakan untuk membaca dari input standar dan menulis ke output standar serta satu atau lebih file. Ini memungkinkan pengguna untuk melihat output dari suatu perintah sambil juga menyimpannya ke dalam file.

## Usage
Sintaks dasar dari perintah `tee` adalah sebagai berikut:

```bash
tee [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan `tee`:

- `-a`, `--append`: Menambahkan output ke file yang sudah ada, bukan menimpanya.
- `-i`, `--ignore-interrupts`: Mengabaikan sinyal interupsi.
- `-p`, `--output-error`: Menentukan bagaimana kesalahan output ditangani.

## Common Examples
Berikut adalah beberapa contoh praktis penggunaan `tee`:

1. Menyimpan output dari perintah ke dalam file:
   ```bash
   ls -l | tee daftar_file.txt
   ```

2. Menyimpan output dan juga menampilkannya di layar:
   ```bash
   echo "Halo, Dunia!" | tee output.txt
   ```

3. Menambahkan output ke file yang sudah ada:
   ```bash
   echo "Baris baru" | tee -a output.txt
   ```

4. Menggunakan `tee` dengan perintah lain dalam pipeline:
   ```bash
   ps aux | grep bash | tee bash_processes.txt
   ```

## Tips
- Gunakan opsi `-a` jika Anda ingin menambahkan output ke file yang sudah ada tanpa menghapus isinya.
- Pertimbangkan untuk menggunakan `tee` dalam skrip untuk mencatat log output sambil tetap menampilkan hasil di terminal.
- Jika Anda tidak ingin output ditampilkan di layar, Anda bisa mengarahkan output ke `/dev/null`:
  ```bash
  command | tee output.txt > /dev/null
  ```