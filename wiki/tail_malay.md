# [Linux] Bash tail Penggunaan: Menunjukkan baris terakhir dari fail

## Overview
Perintah `tail` dalam Bash digunakan untuk memaparkan baris terakhir dari satu atau lebih fail. Ia sangat berguna untuk melihat log fail atau output yang sedang berjalan, membolehkan pengguna mendapatkan maklumat terkini dengan cepat.

## Usage
Sintaks asas untuk perintah `tail` adalah seperti berikut:

```bash
tail [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa yang boleh digunakan dengan perintah `tail`:

- `-n [number]`: Menunjukkan jumlah baris terakhir yang ditentukan. Contohnya, `-n 10` untuk menunjukkan 10 baris terakhir.
- `-f`: Mengikuti fail secara langsung, memaparkan baris baru yang ditambah ke dalam fail secara masa nyata.
- `-c [number]`: Menunjukkan jumlah bait terakhir yang ditentukan.
- `--help`: Menunjukkan bantuan untuk perintah `tail`.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `tail`:

1. Menunjukkan 10 baris terakhir dari fail `log.txt`:
   ```bash
   tail log.txt
   ```

2. Menunjukkan 20 baris terakhir dari fail `data.csv`:
   ```bash
   tail -n 20 data.csv
   ```

3. Mengikuti fail log secara langsung untuk melihat kemas kini baru:
   ```bash
   tail -f server.log
   ```

4. Menunjukkan 50 bait terakhir dari fail `output.txt`:
   ```bash
   tail -c 50 output.txt
   ```

## Tips
- Gunakan `tail -f` untuk memantau fail log secara langsung, sangat berguna untuk debugging aplikasi.
- Anda boleh menggabungkan `tail` dengan perintah lain menggunakan pipe (`|`) untuk analisis lanjut, seperti `tail -n 100 log.txt | grep "ERROR"`.
- Jika anda ingin menghentikan pemantauan fail dengan `tail -f`, tekan `Ctrl + C`.