# [Linux] Bash watch Penggunaan: Memantau Perintah Secara Berkala

## Overview
Perintah `watch` digunakan untuk menjalankan perintah tertentu secara berkala dan menampilkan hasilnya di terminal. Ini sangat berguna untuk memantau perubahan dalam output perintah tanpa perlu menjalankannya secara manual berulang kali.

## Usage
Sintaks dasar dari perintah `watch` adalah sebagai berikut:

```bash
watch [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan perintah `watch`:

- `-n <seconds>`: Menentukan interval waktu dalam detik antara setiap eksekusi perintah.
- `-d`: Menyoroti perbedaan antara output sebelumnya dan output saat ini.
- `-t`: Menonaktifkan tampilan header yang menunjukkan perintah yang sedang dijalankan.

## Common Examples
Berikut adalah beberapa contoh praktis penggunaan perintah `watch`:

1. Memantau penggunaan CPU setiap 2 detik:
   ```bash
   watch -n 2 cpu -l
   ```

2. Memantau status direktori dengan `ls`:
   ```bash
   watch ls -l
   ```

3. Memantau penggunaan disk dengan `df`:
   ```bash
   watch -d df -h
   ```

4. Memantau proses yang berjalan dengan `ps`:
   ```bash
   watch -n 5 'ps aux | grep httpd'
   ```

## Tips
- Gunakan opsi `-d` untuk lebih mudah melihat perubahan dalam output.
- Sesuaikan interval waktu dengan `-n` agar tidak terlalu sering menjalankan perintah, yang dapat membebani sistem.
- Pertimbangkan untuk menggunakan tanda kutip pada perintah yang memiliki spasi atau karakter khusus untuk menghindari kesalahan.