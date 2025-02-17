# [Linux] Bash parted Penggunaan: Mengelola Partisi Disk

## Overview
Perintah `parted` adalah alat yang digunakan untuk mengelola partisi pada disk. Dengan `parted`, pengguna dapat membuat, menghapus, dan mengubah ukuran partisi, serta melakukan berbagai operasi lain yang berkaitan dengan manajemen partisi.

## Usage
Berikut adalah sintaks dasar dari perintah `parted`:

```bash
parted [options] [arguments]
```

## Common Options
- `-l`, `--list`: Menampilkan daftar semua disk dan partisi yang ada.
- `-s`, `--script`: Menjalankan perintah dalam mode skrip tanpa meminta konfirmasi.
- `mkpart`: Membuat partisi baru.
- `rm`: Menghapus partisi yang ada.
- `resizepart`: Mengubah ukuran partisi yang ada.

## Common Examples
Berikut adalah beberapa contoh penggunaan `parted`:

1. **Menampilkan daftar partisi:**
   ```bash
   parted -l
   ```

2. **Membuat partisi baru:**
   ```bash
   parted /dev/sda mkpart primary ext4 1MiB 100MiB
   ```

3. **Menghapus partisi:**
   ```bash
   parted /dev/sda rm 1
   ```

4. **Mengubah ukuran partisi:**
   ```bash
   parted /dev/sda resizepart 1 200MiB
   ```

## Tips
- Selalu cadangkan data penting sebelum melakukan perubahan pada partisi.
- Gunakan opsi `--script` jika Anda menjalankan `parted` dalam skrip untuk menghindari prompt konfirmasi.
- Pastikan untuk memeriksa jenis sistem file yang digunakan pada partisi sebelum melakukan operasi yang dapat mempengaruhi data.