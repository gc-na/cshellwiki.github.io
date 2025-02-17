# [Linux] Bash fc Penggunaan: Mengedit dan menjalankan perintah sebelumnya

## Overview
Perintah `fc` dalam Bash digunakan untuk mengedit dan menjalankan kembali perintah-perintah yang telah dieksekusi sebelumnya. Ini sangat berguna ketika Anda ingin memperbaiki kesalahan atau mengubah perintah yang telah Anda jalankan tanpa harus mengetik ulang semuanya.

## Usage
Berikut adalah sintaks dasar dari perintah `fc`:

```
fc [options] [arguments]
```

## Common Options
- `-l`: Menampilkan daftar perintah yang telah dieksekusi sebelumnya.
- `-r`: Menjalankan perintah dalam urutan terbalik.
- `-s`: Menjalankan perintah terakhir tanpa membuka editor.
- `-n`: Menampilkan nomor perintah saat menggunakan opsi `-l`.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `fc`:

1. **Menampilkan daftar perintah sebelumnya:**
   ```bash
   fc -l
   ```

2. **Mengedit perintah terakhir yang dijalankan:**
   ```bash
   fc
   ```

3. **Menjalankan perintah terakhir tanpa mengedit:**
   ```bash
   fc -s
   ```

4. **Menampilkan daftar perintah sebelumnya dengan nomor:**
   ```bash
   fc -ln -5
   ```

5. **Mengedit perintah tertentu dari daftar:**
   ```bash
   fc 10
   ```

## Tips
- Gunakan `fc` secara rutin untuk memperbaiki kesalahan kecil dalam perintah yang baru saja Anda jalankan.
- Anda dapat menggabungkan `fc` dengan editor teks favorit Anda dengan mengatur variabel `EDITOR`.
- Cobalah menggunakan opsi `-r` untuk menjalankan perintah dalam urutan terbalik jika Anda sering menggunakan perintah yang sama.