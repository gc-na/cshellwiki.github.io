# [Linux] Bash fdisk Penggunaan: Mengelola Partisi Disk

## Overview
Perintah `fdisk` adalah alat yang digunakan untuk mengelola tabel partisi disk pada sistem operasi berbasis Linux. Dengan `fdisk`, pengguna dapat membuat, menghapus, dan mengubah ukuran partisi pada hard disk atau media penyimpanan lainnya.

## Usage
Berikut adalah sintaks dasar dari perintah `fdisk`:

```
fdisk [options] [arguments]
```

## Common Options
- `-l`: Menampilkan semua partisi yang ada pada disk.
- `-u`: Menggunakan ukuran sektor dalam satuan sektor.
- `-n`: Membuat partisi baru.
- `-d`: Menghapus partisi yang ada.
- `-s`: Menampilkan ukuran partisi.

## Common Examples
Berikut adalah beberapa contoh penggunaan `fdisk`:

1. **Menampilkan daftar partisi pada disk:**
   ```bash
   fdisk -l
   ```

2. **Membuat partisi baru:**
   ```bash
   fdisk /dev/sda
   ```
   Setelah menjalankan perintah ini, Anda akan masuk ke mode interaktif `fdisk`, di mana Anda dapat menggunakan perintah seperti `n` untuk membuat partisi baru.

3. **Menghapus partisi:**
   ```bash
   fdisk /dev/sda
   ```
   Masuk ke mode interaktif dan gunakan perintah `d` untuk menghapus partisi yang diinginkan.

4. **Menampilkan ukuran partisi:**
   ```bash
   fdisk -s /dev/sda1
   ```

## Tips
- Selalu cadangkan data penting sebelum melakukan perubahan pada partisi untuk menghindari kehilangan data.
- Gunakan perintah `man fdisk` untuk mendapatkan informasi lebih lanjut tentang opsi dan penggunaannya.
- Pastikan Anda memiliki hak akses yang diperlukan (biasanya sebagai root) untuk melakukan perubahan pada partisi.