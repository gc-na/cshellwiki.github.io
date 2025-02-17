# [Linux] Bash mount penggunaan: Mengaitkan sistem file

## Overview
Perintah `mount` digunakan untuk mengaitkan sistem file ke dalam direktori tertentu di sistem Linux. Dengan menggunakan perintah ini, Anda dapat mengakses file dan direktori dari perangkat penyimpanan yang berbeda, seperti hard drive, USB, atau partisi lainnya.

## Usage
Berikut adalah sintaks dasar dari perintah `mount`:

```bash
mount [options] [arguments]
```

## Common Options
- `-t` : Menentukan jenis sistem file yang akan dipasang.
- `-o` : Menentukan opsi tambahan saat memasang sistem file.
- `-a` : Memasang semua sistem file yang terdaftar di `/etc/fstab`.
- `-r` : Memasang sistem file dalam mode baca saja.
- `-w` : Memasang sistem file dalam mode baca-tulis.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `mount`:

1. **Memasang sistem file dari perangkat**:
   ```bash
   mount /dev/sdb1 /mnt/usb
   ```
   Contoh ini memasang partisi USB yang terletak di `/dev/sdb1` ke direktori `/mnt/usb`.

2. **Memasang sistem file dengan jenis tertentu**:
   ```bash
   mount -t ext4 /dev/sda1 /mnt/data
   ```
   Di sini, kita memasang partisi yang menggunakan sistem file `ext4` ke direktori `/mnt/data`.

3. **Memasang sistem file dalam mode baca saja**:
   ```bash
   mount -o ro /dev/sdc1 /mnt/read_only
   ```
   Perintah ini memasang partisi `/dev/sdc1` dalam mode baca saja ke direktori `/mnt/read_only`.

4. **Memasang semua sistem file yang terdaftar di fstab**:
   ```bash
   mount -a
   ```
   Dengan perintah ini, semua sistem file yang terdaftar di file konfigurasi `/etc/fstab` akan dipasang secara otomatis.

## Tips
- Selalu pastikan bahwa direktori tujuan sudah ada sebelum menggunakan perintah `mount`.
- Gunakan opsi `-o ro` jika Anda hanya perlu membaca data dari sistem file tanpa mengubahnya.
- Setelah selesai menggunakan sistem file, jangan lupa untuk melepasnya dengan perintah `umount` untuk menghindari kehilangan data.