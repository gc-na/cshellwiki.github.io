# [Linux] Bash exit Penggunaan: Mengakhiri proses shell

## Overview
Perintah `exit` digunakan dalam Bash untuk mengakhiri sesi shell atau skrip. Ketika perintah ini dijalankan, shell akan keluar dan mengembalikan status keluar yang ditentukan. Status keluar ini berguna untuk menunjukkan apakah proses berjalan dengan sukses atau mengalami kesalahan.

## Usage
Berikut adalah sintaks dasar dari perintah `exit`:

```
exit [options] [status]
```

## Common Options
- `status`: Angka yang menunjukkan status keluar. Jika tidak ditentukan, status terakhir yang dijalankan akan digunakan.

## Common Examples

1. **Keluar dari shell dengan status default:**
   ```bash
   exit
   ```

2. **Keluar dari shell dengan status tertentu (misalnya, 0 untuk sukses):**
   ```bash
   exit 0
   ```

3. **Keluar dari skrip dengan status kesalahan (misalnya, 1):**
   ```bash
   exit 1
   ```

4. **Menggunakan exit dalam skrip:**
   ```bash
   #!/bin/bash
   echo "Menjalankan skrip..."
   if [ ! -f "file.txt" ]; then
       echo "File tidak ditemukan!"
       exit 1
   fi
   echo "Skrip selesai."
   exit 0
   ```

## Tips
- Selalu gunakan status keluar yang sesuai untuk menunjukkan hasil dari skrip Anda. Status 0 menunjukkan keberhasilan, sedangkan angka lainnya menunjukkan kesalahan.
- Dalam skrip yang lebih kompleks, pertimbangkan untuk menggunakan variabel untuk menyimpan status keluar sebelum menggunakan perintah `exit`.
- Jika Anda menggunakan `exit` dalam subshell, ingat bahwa itu hanya akan keluar dari subshell tersebut, bukan dari shell utama.