# [Sistem Operasi] C Shell (csh) strace Penggunaan: Melacak sistem panggilan

## Overview
Perintah `strace` digunakan untuk melacak sistem panggilan dan sinyal yang diterima oleh proses yang sedang berjalan. Ini sangat berguna untuk debugging dan menganalisis bagaimana program berinteraksi dengan kernel sistem operasi.

## Usage
Sintaks dasar dari perintah `strace` adalah sebagai berikut:

```csh
strace [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum untuk `strace` beserta penjelasannya:

- `-c`: Menghitung statistik sistem panggilan.
- `-e trace=<syscall>`: Melacak hanya sistem panggilan tertentu.
- `-o <file>`: Menyimpan output ke dalam file yang ditentukan.
- `-p <pid>`: Melacak proses yang sudah berjalan dengan ID proses tertentu.
- `-f`: Mengikuti proses anak yang dibuat oleh proses yang dilacak.

## Common Examples
Berikut adalah beberapa contoh praktis penggunaan `strace`:

1. Melacak semua sistem panggilan dari program `ls`:
   ```csh
   strace ls
   ```

2. Menghitung statistik sistem panggilan:
   ```csh
   strace -c ls
   ```

3. Melacak hanya sistem panggilan `open`:
   ```csh
   strace -e trace=open ls
   ```

4. Menyimpan output ke dalam file:
   ```csh
   strace -o output.txt ls
   ```

5. Melacak proses yang sudah berjalan dengan ID 1234:
   ```csh
   strace -p 1234
   ```

## Tips
- Gunakan opsi `-c` untuk mendapatkan ringkasan statistik setelah menjalankan perintah, ini membantu dalam analisis cepat.
- Jika Anda hanya tertarik pada sistem panggilan tertentu, gunakan opsi `-e trace=<syscall>` untuk mempersempit fokus.
- Simpan output ke file dengan opsi `-o` jika Anda perlu menganalisis hasilnya lebih lanjut atau membagikannya dengan orang lain.