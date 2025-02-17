# [Linux] Bash di at: Menjadwalkan tugas sekali

## Overview
Perintah `at` digunakan untuk menjadwalkan tugas yang akan dilaksanakan pada waktu tertentu di masa depan. Dengan `at`, pengguna dapat menjalankan skrip atau perintah tanpa perlu mengawasi secara langsung.

## Usage
Sintaks dasar untuk menggunakan perintah `at` adalah seperti berikut:

```
at [options] [arguments]
```

## Common Options
- `-f FILE`: Mengambil perintah dari fail yang ditentukan.
- `-m`: Menghantar e-mel kepada pengguna setelah tugas selesai.
- `-q QUEUE`: Menentukan barisan untuk tugas yang dijadwalkan.
- `-V`: Menunjukkan versi `at` yang sedang digunakan.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `at`:

1. Menjadwalkan perintah untuk dijalankan pada waktu tertentu:
   ```bash
   echo "echo 'Hello, World!'" | at 14:00
   ```

2. Menjadwalkan skrip untuk dijalankan pada hari tertentu:
   ```bash
   at 09:00 2023-10-25 < myscript.sh
   ```

3. Menggunakan pilihan `-m` untuk menghantar e-mel setelah tugas selesai:
   ```bash
   echo "backup.sh" | at -m now + 1 hour
   ```

4. Menjadwalkan perintah untuk dijalankan pada waktu yang ditentukan menggunakan format waktu relatif:
   ```bash
   echo "shutdown now" | at now + 5 minutes
   ```

## Tips
- Pastikan perkhidmatan `atd` sedang berjalan untuk menjadwalkan tugas.
- Gunakan `atq` untuk menyemak senarai tugas yang telah dijadwalkan.
- Untuk membatalkan tugas yang telah dijadwalkan, gunakan `atrm` diikuti dengan ID tugas yang ingin dibatalkan.