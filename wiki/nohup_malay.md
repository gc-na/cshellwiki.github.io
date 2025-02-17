# [Linux] Bash nohup Penggunaan: Menjalankan proses tanpa gangguan

## Overview
Perintah `nohup` (no hang up) digunakan dalam Bash untuk menjalankan proses yang tidak akan terhenti walaupun sesi terminal ditutup. Ini sangat berguna untuk menjalankan aplikasi jangka panjang yang perlu terus berjalan tanpa gangguan.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `nohup`:

```
nohup [options] [arguments]
```

## Common Options
- `&` : Menjalankan proses di latar belakang.
- `-h` : Menunjukkan bantuan untuk perintah nohup.
- `-v` : Menunjukkan versi dari nohup.

## Common Examples
Berikut adalah beberapa contoh penggunaan `nohup`:

1. Menjalankan skrip shell di latar belakang:
   ```bash
   nohup ./myscript.sh &
   ```

2. Menjalankan perintah `ping` dan menyimpan output ke dalam fail:
   ```bash
   nohup ping google.com > output.txt &
   ```

3. Menjalankan aplikasi Python:
   ```bash
   nohup python myapp.py &
   ```

4. Menjalankan perintah dengan output ke fail dan menutup terminal:
   ```bash
   nohup java -jar myapp.jar > app.log 2>&1 &
   ```

## Tips
- Selalu gunakan `&` di akhir perintah untuk menjalankan proses di latar belakang.
- Periksa fail `nohup.out` untuk melihat output jika tidak mengarahkan ke fail lain.
- Gunakan `jobs` untuk melihat proses latar belakang yang sedang berjalan.