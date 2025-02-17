# [Linux] Bash pidstat Penggunaan: Memantau Statistik Proses

## Overview
Perintah `pidstat` digunakan untuk memantau statistik penggunaan sumber daya sistem oleh proses yang sedang berjalan. Ini memberikan informasi tentang penggunaan CPU, memori, dan statistik lainnya untuk setiap proses yang terdaftar.

## Usage
Sintaks dasar dari perintah `pidstat` adalah sebagai berikut:

```
pidstat [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan `pidstat`:

- `-h`: Menampilkan header yang lebih jelas.
- `-r`: Menampilkan statistik penggunaan memori.
- `-u`: Menampilkan statistik penggunaan CPU.
- `-p <pid>`: Memantau proses tertentu berdasarkan ID proses.
- `-t`: Menampilkan statistik untuk semua thread dalam proses.

## Common Examples

1. **Memantau Penggunaan CPU untuk Semua Proses**
   ```bash
   pidstat -u
   ```

2. **Menampilkan Statistik Memori untuk Proses Tertentu**
   ```bash
   pidstat -r -p 1234
   ```

3. **Memantau Semua Thread dalam Proses**
   ```bash
   pidstat -t -p 5678
   ```

4. **Menampilkan Statistik dengan Header yang Jelas**
   ```bash
   pidstat -h -u
   ```

5. **Memantau Penggunaan CPU Setiap 2 Detik**
   ```bash
   pidstat -u 2
   ```

## Tips
- Gunakan opsi `-h` untuk memudahkan pembacaan output, terutama saat memantau banyak proses.
- Jika Anda hanya tertarik pada satu proses, gunakan opsi `-p` untuk mempersempit fokus dan mengurangi kebisingan informasi.
- Pertimbangkan untuk menggabungkan `pidstat` dengan perintah lain seperti `grep` untuk memfilter output sesuai kebutuhan Anda.