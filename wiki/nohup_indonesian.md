# [Linux] Bash nohup Penggunaan: Menjalankan proses tanpa terganggu

## Overview
Perintah `nohup` digunakan untuk menjalankan proses di latar belakang yang tidak akan terpengaruh oleh logout pengguna. Dengan menggunakan `nohup`, proses yang dijalankan akan tetap berjalan meskipun sesi terminal ditutup.

## Usage
Sintaks dasar dari perintah `nohup` adalah sebagai berikut:

```
nohup [options] [arguments]
```

## Common Options
- `&` : Menjalankan proses di latar belakang.
- `-h` : Menampilkan bantuan tentang penggunaan `nohup`.
- `-v` : Menampilkan versi dari `nohup`.

## Common Examples
Berikut adalah beberapa contoh penggunaan `nohup`:

1. Menjalankan skrip shell di latar belakang:
   ```bash
   nohup ./myscript.sh &
   ```

2. Menjalankan perintah `ping` untuk menguji koneksi tanpa terputus:
   ```bash
   nohup ping google.com &
   ```

3. Menyimpan output dari perintah ke dalam file log:
   ```bash
   nohup ./myapp > output.log 2>&1 &
   ```

## Tips
- Selalu gunakan `&` di akhir perintah untuk memastikan proses berjalan di latar belakang.
- Periksa file `nohup.out` untuk melihat output dari proses yang dijalankan jika tidak ditentukan file output lain.
- Gunakan perintah `jobs` untuk melihat proses yang sedang berjalan di latar belakang.