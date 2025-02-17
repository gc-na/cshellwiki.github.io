# [Linux] Bash history Penggunaan: Menampilkan riwayat perintah

## Overview
Perintah `history` dalam Bash digunakan untuk menampilkan daftar perintah yang telah dieksekusi sebelumnya dalam sesi terminal. Ini sangat berguna untuk mengingat dan mengulangi perintah yang sering digunakan tanpa harus mengetiknya lagi.

## Usage
Sintaks dasar dari perintah `history` adalah sebagai berikut:

```
history [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum untuk perintah `history` beserta penjelasannya:

- `-c`: Menghapus seluruh riwayat perintah.
- `-d offset`: Menghapus perintah pada posisi tertentu dalam riwayat.
- `n`: Menampilkan `n` baris terakhir dari riwayat perintah.

## Common Examples
Berikut adalah beberapa contoh praktis penggunaan perintah `history`:

1. Menampilkan seluruh riwayat perintah:
   ```bash
   history
   ```

2. Menampilkan 10 perintah terakhir:
   ```bash
   history 10
   ```

3. Menghapus seluruh riwayat perintah:
   ```bash
   history -c
   ```

4. Menghapus perintah tertentu dari riwayat (misalnya, perintah ke-5):
   ```bash
   history -d 5
   ```

## Tips
- Gunakan `!n` untuk menjalankan perintah ke-n dari riwayat. Misalnya, `!100` akan menjalankan perintah yang terdaftar sebagai perintah ke-100.
- Untuk mencari perintah sebelumnya, tekan `Ctrl + r` dan mulai ketikkan perintah yang ingin dicari.
- Simpan riwayat perintah ke dalam file dengan menggunakan `history > nama_file.txt` untuk referensi di masa mendatang.