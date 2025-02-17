# [Linux] Bash pidstat Penggunaan: Memantau statistik proses

## Overview
Perintah `pidstat` digunakan untuk memantau dan melaporkan statistik penggunaan sumber daya sistem oleh proses yang sedang berjalan. Ia memberikan maklumat terperinci mengenai penggunaan CPU, memori, dan I/O bagi setiap proses, yang berguna untuk analisis prestasi sistem.

## Usage
Sintaks asas bagi perintah `pidstat` adalah seperti berikut:

```bash
pidstat [options] [arguments]
```

## Common Options
- `-h`: Menunjukkan tajuk yang lebih mudah dibaca.
- `-r`: Memaparkan statistik penggunaan memori.
- `-u`: Memaparkan statistik penggunaan CPU.
- `-p <pid>`: Memantau proses tertentu berdasarkan ID proses (PID).
- `-t`: Memaparkan statistik untuk semua thread dalam proses.

## Common Examples
Berikut adalah beberapa contoh penggunaan `pidstat`:

1. **Memantau penggunaan CPU semua proses:**
   ```bash
   pidstat
   ```

2. **Memantau penggunaan CPU untuk proses tertentu dengan PID 1234:**
   ```bash
   pidstat -p 1234
   ```

3. **Memaparkan statistik penggunaan memori untuk semua proses:**
   ```bash
   pidstat -r
   ```

4. **Memantau penggunaan CPU dan memori setiap 5 saat:**
   ```bash
   pidstat 5
   ```

5. **Memaparkan statistik untuk semua thread dalam proses dengan PID 5678:**
   ```bash
   pidstat -t -p 5678
   ```

## Tips
- Gunakan `pidstat` bersama dengan `grep` untuk mencari proses tertentu dengan lebih mudah.
- Untuk analisis jangka panjang, pertimbangkan untuk menyimpan output `pidstat` ke dalam fail untuk rujukan kemudian.
- Sentiasa semak pilihan yang ada dengan `man pidstat` untuk memahami lebih lanjut tentang fungsi dan opsyen yang tersedia.