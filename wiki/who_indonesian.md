# [Linux] Bash who Penggunaan: Menampilkan pengguna yang sedang masuk

## Overview
Perintah `who` digunakan untuk menampilkan daftar pengguna yang sedang masuk ke sistem. Informasi yang ditampilkan termasuk nama pengguna, terminal yang digunakan, waktu login, dan alamat IP atau hostname jika tersedia.

## Usage
Sintaks dasar dari perintah `who` adalah sebagai berikut:

```bash
who [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang dapat digunakan dengan perintah `who`:

- `-a`: Menampilkan semua informasi yang tersedia, termasuk pengguna yang tidak aktif.
- `-b`: Menampilkan waktu terakhir sistem di-boot.
- `-q`: Menampilkan hanya nama pengguna yang sedang masuk dan jumlahnya.
- `--help`: Menampilkan bantuan tentang penggunaan perintah `who`.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `who`:

1. Menampilkan daftar pengguna yang sedang masuk:
   ```bash
   who
   ```

2. Menampilkan semua informasi yang tersedia:
   ```bash
   who -a
   ```

3. Menampilkan waktu terakhir sistem di-boot:
   ```bash
   who -b
   ```

4. Menampilkan hanya nama pengguna yang sedang masuk dan jumlahnya:
   ```bash
   who -q
   ```

## Tips
- Gunakan opsi `-a` untuk mendapatkan informasi lebih lengkap tentang pengguna yang sedang aktif dan status terminal mereka.
- Perintah `who` dapat digabungkan dengan perintah lain seperti `grep` untuk mencari pengguna tertentu. Contoh:
  ```bash
  who | grep username
  ```
- Untuk memantau aktivitas pengguna secara real-time, pertimbangkan untuk menggunakan perintah `w` yang memberikan informasi lebih detail tentang aktivitas pengguna.