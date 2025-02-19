# [Sistem Operasi] C Shell (csh) pidstat Penggunaan: Memantau Statistik Proses

## Overview
Perintah `pidstat` digunakan untuk memantau statistik penggunaan sumber daya sistem dari proses yang berjalan. Ini memberikan informasi penting seperti penggunaan CPU, memori, dan I/O untuk setiap proses yang aktif.

## Usage
Sintaks dasar dari perintah `pidstat` adalah sebagai berikut:

```csh
pidstat [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum untuk `pidstat` beserta penjelasannya:

- `-p <pid>`: Menentukan ID proses yang ingin dipantau.
- `-r`: Menampilkan statistik penggunaan memori.
- `-u`: Menampilkan statistik penggunaan CPU.
- `-d`: Menampilkan statistik I/O disk.
- `-h`: Menampilkan informasi dalam format yang lebih mudah dibaca.

## Common Examples
Berikut adalah beberapa contoh penggunaan `pidstat`:

1. Memantau semua proses dengan statistik CPU:
   ```csh
   pidstat -u
   ```

2. Memantau proses tertentu dengan ID 1234:
   ```csh
   pidstat -p 1234
   ```

3. Menampilkan statistik penggunaan memori untuk semua proses:
   ```csh
   pidstat -r
   ```

4. Memantau statistik I/O disk untuk semua proses:
   ```csh
   pidstat -d
   ```

5. Menggunakan opsi `-h` untuk format yang lebih mudah dibaca:
   ```csh
   pidstat -u -h
   ```

## Tips
- Gunakan opsi `-r` dan `-u` secara bersamaan untuk mendapatkan gambaran lengkap tentang penggunaan sumber daya proses.
- Pertimbangkan untuk menjalankan `pidstat` dalam interval waktu tertentu untuk memantau perubahan dalam penggunaan sumber daya.
- Simpan output `pidstat` ke dalam file untuk analisis lebih lanjut dengan menggunakan operator pengalihan (`>`).