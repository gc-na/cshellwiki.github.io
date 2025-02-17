# [Linux] Bash dstat Penggunaan: Memantau sumber daya sistem secara real-time

## Overview
Perintah `dstat` adalah alat yang berguna untuk memantau dan menganalisis penggunaan sumber daya sistem secara real-time. Dengan `dstat`, pengguna dapat melihat berbagai statistik seperti penggunaan CPU, memori, disk, dan jaringan dalam satu tampilan yang mudah dibaca.

## Usage
Berikut adalah sintaks dasar dari perintah `dstat`:

```bash
dstat [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan `dstat`:

- `-c` : Menampilkan penggunaan CPU.
- `-d` : Menampilkan statistik disk.
- `-n` : Menampilkan statistik jaringan.
- `-m` : Menampilkan penggunaan memori.
- `-t` : Menampilkan waktu saat ini.
- `--help` : Menampilkan bantuan dan informasi lebih lanjut tentang penggunaan `dstat`.

## Common Examples
Berikut adalah beberapa contoh penggunaan `dstat`:

1. Menampilkan penggunaan CPU dan memori:
   ```bash
   dstat -c -m
   ```

2. Menampilkan statistik disk dan jaringan:
   ```bash
   dstat -d -n
   ```

3. Menampilkan semua statistik dengan waktu:
   ```bash
   dstat -tcdmn
   ```

4. Menyimpan output ke file untuk analisis lebih lanjut:
   ```bash
   dstat -tcdmn > dstat_output.txt
   ```

## Tips
- Gunakan opsi `-t` untuk menambahkan cap waktu pada output, sehingga Anda dapat melacak perubahan dari waktu ke waktu.
- Pertimbangkan untuk menjalankan `dstat` dengan opsi `--full` untuk mendapatkan informasi yang lebih mendetail.
- Jika Anda ingin memantau sistem secara terus-menerus, Anda dapat menggunakan `dstat` dalam kombinasi dengan `watch` untuk memperbarui tampilan secara berkala:
  ```bash
  watch dstat -tcdmn
  ```