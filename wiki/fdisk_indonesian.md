# [Sistem Operasi] C Shell (csh) fdisk Penggunaan: Mengelola partisi disk

## Overview
Perintah `fdisk` digunakan untuk mengelola partisi pada disk. Dengan `fdisk`, pengguna dapat membuat, menghapus, dan mengubah ukuran partisi, serta melihat informasi tentang partisi yang ada.

## Usage
Berikut adalah sintaks dasar dari perintah `fdisk`:

```csh
fdisk [options] [arguments]
```

## Common Options
- `-l`: Menampilkan daftar semua partisi yang ada pada disk.
- `-n`: Membuat partisi baru.
- `-d`: Menghapus partisi yang ada.
- `-s`: Menampilkan ukuran partisi dalam blok.

## Common Examples
Berikut adalah beberapa contoh penggunaan `fdisk`:

1. **Menampilkan daftar partisi:**
   ```csh
   fdisk -l
   ```

2. **Membuat partisi baru:**
   ```csh
   fdisk -n /dev/sda
   ```

3. **Menghapus partisi:**
   ```csh
   fdisk -d /dev/sda1
   ```

4. **Menampilkan ukuran partisi:**
   ```csh
   fdisk -s /dev/sda1
   ```

## Tips
- Selalu cadangkan data penting sebelum melakukan perubahan pada partisi.
- Gunakan `fdisk` dengan hati-hati, karena kesalahan dapat mengakibatkan kehilangan data.
- Setelah mengubah partisi, pastikan untuk memformat partisi baru sebelum menggunakannya.