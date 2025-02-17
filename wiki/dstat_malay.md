# [Linux] Bash dstat Penggunaan: Memantau sumber sistem secara real-time

## Overview
Perintah `dstat` adalah alat yang berguna untuk memantau sumber sistem secara real-time. Ia menggabungkan fungsi dari beberapa alat pemantauan seperti `vmstat`, `iostat`, dan `netstat`, memberikan pandangan menyeluruh tentang penggunaan CPU, memori, disk, dan jaringan.

## Usage
Sintaks asas untuk menggunakan perintah `dstat` adalah seperti berikut:

```bash
dstat [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan umum yang boleh digunakan dengan `dstat`:

- `-c`: Tunjukkan penggunaan CPU.
- `-d`: Tunjukkan statistik disk.
- `-n`: Tunjukkan statistik rangkaian.
- `-m`: Tunjukkan penggunaan memori.
- `-t`: Tunjukkan cap waktu.
- `--full`: Tunjukkan semua maklumat yang tersedia.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `dstat`:

1. **Menunjukkan penggunaan CPU dan memori:**
   ```bash
   dstat -c -m
   ```

2. **Menunjukkan statistik disk dan rangkaian:**
   ```bash
   dstat -d -n
   ```

3. **Menunjukkan semua maklumat dengan cap waktu:**
   ```bash
   dstat --full -t
   ```

4. **Menunjukkan penggunaan CPU, memori, dan disk secara serentak:**
   ```bash
   dstat -c -m -d
   ```

## Tips
- Gunakan pilihan `--full` untuk mendapatkan gambaran menyeluruh tentang sumber sistem anda.
- Jalankan `dstat` dalam terminal yang berasingan untuk memantau sistem tanpa mengganggu proses lain.
- Simpan output ke dalam fail untuk analisis kemudian dengan menggunakan pengalihan output, contohnya:
  ```bash
  dstat -c -m > dstat_output.txt
  ```