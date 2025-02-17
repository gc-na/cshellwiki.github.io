# [Linux] Bash strace Penggunaan: Melacak panggilan sistem dan sinyal

## Overview
Perintah `strace` digunakan untuk melacak panggilan sistem yang dilakukan oleh proses dan sinyal yang diterima oleh proses tersebut. Ini sangat berguna untuk debugging aplikasi dan memahami interaksi antara program dan kernel.

## Usage
Sintaks dasar dari perintah `strace` adalah sebagai berikut:

```bash
strace [options] [arguments]
```

## Common Options
- `-o <file>`: Menyimpan output ke dalam file yang ditentukan.
- `-e <expression>`: Menentukan jenis panggilan sistem yang ingin dilacak.
- `-p <pid>`: Melacak proses yang sedang berjalan berdasarkan ID proses (PID).
- `-c`: Menampilkan statistik ringkasan dari panggilan sistem yang dilakukan.
- `-f`: Mengikuti proses anak yang dibuat oleh proses yang dilacak.

## Common Examples
Berikut adalah beberapa contoh penggunaan `strace`:

1. Melacak panggilan sistem dari perintah `ls` dan menampilkan output di terminal:
   ```bash
   strace ls
   ```

2. Menyimpan output `strace` ke dalam file bernama `output.txt`:
   ```bash
   strace -o output.txt ls
   ```

3. Melacak proses yang sudah berjalan dengan PID 1234:
   ```bash
   strace -p 1234
   ```

4. Menghitung statistik panggilan sistem yang dilakukan oleh perintah `sleep`:
   ```bash
   strace -c sleep 1
   ```

5. Melacak hanya panggilan sistem yang berkaitan dengan file:
   ```bash
   strace -e trace=file ls
   ```

## Tips
- Gunakan opsi `-o` untuk menyimpan hasil pelacakan ke dalam file agar lebih mudah dianalisis.
- Kombinasikan opsi `-e` dengan `-f` untuk melacak proses anak secara bersamaan.
- Jika Anda hanya tertarik pada kesalahan, gunakan opsi `-e trace=error` untuk fokus pada panggilan sistem yang gagal.
- Pastikan untuk menjalankan `strace` dengan hak akses yang sesuai, terutama saat melacak proses yang memerlukan izin root.