# [Linux] C Shell (csh) parted Penggunaan: Mengelola partisi disk

## Overview
Perintah `parted` digunakan untuk mengelola partisi disk pada sistem operasi berbasis Unix. Dengan `parted`, pengguna dapat membuat, menghapus, dan mengubah ukuran partisi dengan mudah.

## Usage
Berikut adalah sintaks dasar dari perintah `parted`:

```bash
parted [options] [arguments]
```

## Common Options
- `-l`, `--list`: Menampilkan daftar semua disk dan partisi yang ada.
- `-s`, `--script`: Menjalankan perintah tanpa interaksi pengguna.
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
- Gunakan opsi `-s` untuk menjalankan perintah tanpa konfirmasi jika Anda yakin dengan tindakan yang akan diambil.
- Periksa sistem file pada partisi sebelum mengubah ukuran dengan menggunakan perintah `fsck`.